1. **Router**: Connects multiple networks, directing data packets between them. It manages traffic and provides access to the internet.
2. **Switch**: Connects devices within a single network, using MAC addresses to forward data to the correct destination. It operates at the data link layer (Layer 2).
3. **Hub**: A basic networking device that connects multiple Ethernet devices, making them act as a single network segment. It broadcasts data to all ports, which can lead to collisions.
4. **Access Point (AP)**: Extends a wired network by adding Wi-Fi capability, allowing wireless devices to connect to the network.
5. **Firewall**: Monitors and controls incoming and outgoing network traffic based on predetermined security rules. It can be hardware-based or software-based.
6. **Modem**: Modulates and demodulates signals for data transmission over telephone lines, cable systems, or satellite connections, enabling internet access.
7. **Network Interface Card (NIC)**: A hardware component that allows devices to connect to a network, either wired (Ethernet) or wireless (Wi-Fi).
8. **Repeater**: Amplifies and regenerates signals in a network to extend the transmission distance, commonly used in long-distance connections.
9. **Bridge**: Connects two or more network segments, filtering traffic and reducing collisions by dividing traffic into separate collision domains.
10. **Gateway**: Acts as a "gate" between two networks, often with different protocols, enabling communication and data transfer between them.

##### Hub vs. Switch vs. Router

| **Category**         | **Hub**                         | **Switch**                                  | **Router**                                                      |
| -------------------- | ------------------------------- | ------------------------------------------- | --------------------------------------------------------------- |
| **Layer**            | Physical layer (L1)             | Data link layer (L2)                        | Network layer (L3)                                              |
| **Function**         | Blindly broadcasts to all ports | Forwards frames based on MAC addresses/VLAN | Routes packets based on IP addresses (supports NAT/VPN/WiFi AP) |
| **Data Stored**      | None                            | MAC address table (maps MAC to ports)       | IP routing table (subnet routes)                                |
| **Traffic Changes**  | None                            | None                                        | Modifies TTL & checksum in IPv4 header                          |
| **Broadcast Domain** | Single broadcast domain         | One per VLAN                                | Separate domain per interface                                   |
| **Ports**            | 4/12 ports                      | 4–48 ports                                  | 2/4/5/8 ports                                                   |
| **Delivery**         | Bits                            | Frames                                      | Packets                                                         |
| **Duplex Mode**      | Half duplex                     | Half/Full duplex                            | Full duplex                                                     |
