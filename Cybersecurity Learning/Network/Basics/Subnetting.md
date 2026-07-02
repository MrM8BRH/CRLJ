Network subnetting is the practice of dividing a larger network into smaller, more manageable sub-networks (subnets). Subnetting enhances network performance, improves security, and optimizes IP address allocation. It involves borrowing bits from the host portion of an IP address to create additional networks. Subnetting is particularly useful in large networks where traffic needs to be segmented, or when there is a need to efficiently utilize available IP addresses.
### **Key Concepts of Subnetting**
1. **IP Address Structure**  
    An IP address consists of two parts:
    - **Network portion**: Identifies the specific network.
    - **Host portion**: Identifies the specific device (host) within that network.
    The **subnet mask** defines how many bits are allocated to the network portion and how many are left for the host portion.
    - **Example**:
        - IP Address: `192.168.1.10`
        - Subnet Mask: `255.255.255.0`
        - Here, the first 24 bits (the `255.255.255` part) represent the network, and the last 8 bits represent the host.
2. **Subnet Mask**  
    The subnet mask is a 32-bit number that divides an IP address into the network and host parts. The subnet mask is typically represented in dotted decimal format, like `255.255.255.0`, or in CIDR (Classless Inter-Domain Routing) notation, such as `/24`.
    - **Example**:
        - Subnet Mask: `255.255.255.0` (or `/24`)
        - This means 24 bits are used for the network portion, leaving 8 bits for the host portion.
3. **CIDR Notation**  
    CIDR notation is a compact representation of the IP address and subnet mask. It indicates the number of bits used for the network portion of the IP address.
    - **Example**:
        - IP Address: `192.168.1.0/24`
        - This means that the first 24 bits (`192.168.1`) represent the network, and the remaining 8 bits represent the host.
4. **Subnetting Process**  
    The process of subnetting involves the following steps:
    - **Determine the number of subnets required**: Define how many subnets you need for your network.
    - **Calculate the subnet mask**: Based on the number of subnets needed, calculate how many bits you need to borrow from the host portion.
    - **Create subnets**: Use the new subnet mask to divide the network into subnets.
    - **Assign IP addresses**: Allocate specific IP ranges to each subnet.
    **Example**:  
    You have a `192.168.1.0/24` network and need to create 4 subnets.
    - Borrow 2 bits from the host portion (since 2^2 = 4 subnets).
    - New subnet mask becomes `255.255.255.192` or `/26`.
    - This results in 4 subnets, each with 62 usable IP addresses.
### **Important Terms in Subnetting**
1. **Subnet Size**  
    The subnet size refers to the number of available host IP addresses in a subnet.
    - **Formula**: The number of available host addresses = 2^n - 2 (where n is the number of bits left for the host portion).
    - The `-2` accounts for the network address and the broadcast address, which cannot be assigned to hosts.
    - **Example**:
        - Subnet Mask: `255.255.255.192` (/26)
        - Usable IPs = 2^6 - 2 = 62 (usable addresses for hosts).
2. **Network Address**  
    The network address identifies the subnet itself and cannot be assigned to a host. It is the first IP address in the subnet.
    - **Example**: For the subnet `192.168.1.0/26`, the network address is `192.168.1.0`.
3. **Broadcast Address**  
    The broadcast address is used to send data to all devices within the subnet. It is the last IP address in the subnet and also cannot be assigned to a host.
    - **Example**: For the subnet `192.168.1.0/26`, the broadcast address is `192.168.1.63`.
4. **Usable Host IP Range**  
    The usable IP range consists of all IP addresses between the network and broadcast addresses that can be assigned to hosts.
    - **Example**: For the subnet `192.168.1.0/26`, the usable range is from `192.168.1.1` to `192.168.1.62`.
### **Example of Subnetting a Network**
Given the network `192.168.1.0/24`, let’s subnet it into 4 smaller subnets.
1. **Original Network**:
    - IP Address: `192.168.1.0/24`
    - Subnet Mask: `255.255.255.0`
2. **Determine New Subnet Mask**:  
    To create 4 subnets, we need to borrow 2 bits from the host portion (since 2^2 = 4).
    - New Subnet Mask: `255.255.255.192` or `/26`
3. **Divide the Network**:  
    Subnetting with the new mask `/26` gives us 4 subnets:
    - `192.168.1.0/26` (Network Address: `192.168.1.0`, Broadcast Address: `192.168.1.63`, Usable IP Range: `192.168.1.1 - 192.168.1.62`)
    - `192.168.1.64/26` (Network Address: `192.168.1.64`, Broadcast Address: `192.168.1.127`, Usable IP Range: `192.168.1.65 - 192.168.1.126`)
    - `192.168.1.128/26` (Network Address: `192.168.1.128`, Broadcast Address: `192.168.1.191`, Usable IP Range: `192.168.1.129 - 192.168.1.190`)
    - `192.168.1.192/26` (Network Address: `192.168.1.192`, Broadcast Address: `192.168.1.255`, Usable IP Range: `192.168.1.193 - 192.168.1.254`)
4. **Assign IPs**:
    - Each subnet can now accommodate up to 62 hosts, with the first and last IP addresses reserved for network and broadcast addresses, respectively.
### **Benefits of Subnetting**
1. **Improved Network Efficiency**: By dividing large networks into smaller subnets, you can reduce network congestion and improve performance.
2. **Enhanced Security**: Subnetting allows you to isolate parts of your network, making it easier to secure sensitive data and control access.
3. **Better IP Address Management**: Subnetting helps you make more efficient use of available IP addresses, especially in large networks with many devices.
