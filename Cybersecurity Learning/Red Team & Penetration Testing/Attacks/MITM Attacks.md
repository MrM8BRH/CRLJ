MITM attacks occur when an attacker intercepts, monitors, or alters communications between two parties without their knowledge. Below is a breakdown of **common MITM techniques** and their mitigation strategies.
## Top MITM Attack Techniques

| **Technique**              | **Description**                                                                | **Common Targets**                 |
| -------------------------- | ------------------------------------------------------------------------------ | ---------------------------------- |
| **1. ARP Spoofing**        | Attacker sends fake ARP messages to link their MAC address to a legitimate IP. | Local networks (LANs).             |
| **2. DNS Spoofing**        | Corrupts DNS cache to redirect users to malicious sites.                       | Web traffic, login portals.        |
| **3. SSL/TLS Stripping**   | Downgrades HTTPS to HTTP to intercept unencrypted traffic.                     | Secure web sessions.               |
| **4. Wi-Fi Eavesdropping** | Rogue hotspots or packet sniffing on unsecured Wi-Fi.                          | Public Wi-Fi users.                |
| **5. Session Hijacking**   | Steals session cookies or tokens to impersonate authenticated users.           | Web applications, banking sites.   |
| **6. IP Spoofing**         | Masquerades as a trusted IP address to intercept traffic.                      | TCP/IP-based communications.       |
| **7. BGP Hijacking**       | Exploits Border Gateway Protocol to reroute internet traffic.                  | ISP-level traffic, cloud services. |
| **8. Man-in-the-Browser**  | Malware modifies browser activity to alter transactions.                       | Online banking, e-commerce.        |
| **9. HTTPS Spoofing**      | Fake SSL certificates or domains mimicking trusted sites (e.g., `g00gle.com`). | HTTPS-enabled websites.            |
| **10. Email Hijacking**    | Intercepts emails to alter payment details or steal data.                      | Business communications.           |
| **11. Bluetooth MITM**     | Exploits Bluetooth vulnerabilities to intercept device data.                   | IoT devices, smartphones.          |
| **12. Evil Twin Attack**   | Fake Wi-Fi network mimicking a legitimate hotspot.                             | Public Wi-Fi users.                |
| **13. ICMP Redirect**      | Sends false ICMP redirect messages to reroute traffic.                         | Routed networks.                   |
## Detection & Prevention Strategies
### **Detection**  
- **Network Monitoring**: Tools like Wireshark to detect ARP anomalies or unexpected traffic.  
- **Certificate Checks**: Validate SSL/TLS certificates for authenticity (e.g., certificate pinning).  
- **DNS Monitoring**: Detect unexpected DNS resolution changes.  
### **Prevention**  
- **Encryption**: Use HTTPS, VPNs, and SSH for all sensitive communications.  
- **ARP Security**: Enable ARP spoofing detection tools (e.g., Arpwatch) or static ARP entries.  
- **Network Segmentation**: Isolate critical systems to limit attack surface.  
- **Multi-Factor Authentication (MFA)**: Mitigates session hijacking risks.  
- **Certificate Authorities (CAs)**: Enforce strict CA validation and HSTS policies.  
- **User Training**: Educate users to avoid public Wi-Fi for sensitive tasks and verify URLs.  
## Key Takeaways  
- **High-Risk Techniques**: ARP/DNS spoofing, SSL stripping, and Evil Twin attacks are among the most prevalent.  
- **Critical Defenses**: Encryption, certificate validation, and network monitoring are essential.  
- **Zero Trust**: Assume networks are hostile; enforce strict access controls and segmentation.  
*MITM attacks exploit trust in communication channels. Proactive security measures and continuous monitoring are vital to thwart these threats.*  
