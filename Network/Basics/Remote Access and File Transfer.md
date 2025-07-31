## Protocol Overviews

### **Telnet (Telecommunication Network)**  
- **Purpose**: Provides unencrypted command-line access to remote devices.  
- **Port**: TCP/23.  
- **Security**: No encryption; credentials and data transmitted in plaintext.  
- **Use Cases**: Legacy systems, internal networks (discouraged in modern environments).  
### **SSH (Secure Shell)**  
- **Purpose**: Encrypted replacement for Telnet, enabling secure remote access and command execution.  
- **Port**: TCP/22.  
- **Security**: Strong encryption (AES, ChaCha20), authentication, and integrity checks.  
- **Use Cases**: Secure server management, tunneling, automation.  
### **FTP (File Transfer Protocol)**  
- **Purpose**: Transfers files between systems over a network.  
- **Ports**: TCP/21 (control), TCP/20 (data).  
- **Security**: No encryption; credentials and files sent in plaintext.  
- **Use Cases**: Non-sensitive file sharing, legacy systems.  
### **SFTP (SSH File Transfer Protocol)**  
- **Purpose**: Secure file transfer over an encrypted SSH connection.  
- **Port**: TCP/22 (uses SSH).  
- **Security**: Inherits SSH's encryption and authentication.  
- **Use Cases**: Secure file transfers, compliance-driven environments.  
## Key Features Comparison

| **Feature**         | **Telnet**                                   | **SSH**                                      | **FTP**                                      | **SFTP**                                     |
|----------------------|----------------------------------------------|----------------------------------------------|----------------------------------------------|----------------------------------------------|
| **Encryption**       | None                                         | AES, ChaCha20, etc.                          | None                                         | AES, ChaCha20 (via SSH)                      |
| **Authentication**   | Plaintext credentials                        | Public/private keys, passwords               | Plaintext credentials                        | SSH keys, passwords                           |
| **Data Integrity**   | No                                           | Yes (HMAC)                                   | No                                           | Yes (via SSH)                                |
| **Ports**            | 23                                           | 22                                           | 20/21                                        | 22                                           |
| **Security Risks**   | High (sniffing, MITM attacks)                | Low (if properly configured)                 | High (sniffing, data leaks)                  | Low (depends on SSH security)                |
| **Use Cases**        | Legacy device management (avoid in production)| Secure remote administration, scripting      | Non-critical file transfers (internal use)   | Secure file transfers, compliance (HIPAA, PCI-DSS) |
| **Compliance**       | Non-compliant                                | Required for secure environments             | Non-compliant                                | Required for secure environments             |
## Summary of Use Cases
- **Telnet**:  
  - Avoid in production. Only for legacy/internal systems with no security requirements.  
- **SSH**:  
  - Default for secure remote access, tunneling, and automation.  
- **FTP**:  
  - Suitable for non-sensitive transfers where simplicity is prioritized (e.g., local networks).  
- **SFTP**:  
  - Secure alternative to FTP; ideal for sensitive data, compliance, and encrypted transfers.  
---
### Key Takeaways:
- **Security**: SSH/SFTP > FTP > Telnet.  
- **Encryption**: SSH and SFTP encrypt all traffic; Telnet/FTP expose data.  
- **Compliance**: SSH and SFTP meet modern standards; Telnet/FTP are obsolete for regulated use.  
*Always prefer SSH/SFTP for secure operations. Use FTP only in isolated, non-sensitive environments.*  
