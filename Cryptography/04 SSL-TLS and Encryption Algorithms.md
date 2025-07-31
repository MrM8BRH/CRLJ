Many people confuse SSL/TLS with encryption algorithms like AES, RSA, or Diffie-Hellman. However, it's important to differentiate protocols from encryption algorithms. 
**Definition:** 
- SSL/TLS Protocol: A protocol that provides secure communication over a network. 
- Encryption Algorithm: A mathematical function used for encrypting/decrypting data. 
**Purpose:** 
- SSL/TLS Protocol: Ensures secure key exchange, authentication, encryption, integrity, and session management. 
- Encryption Algorithm: Only encrypts and decrypts data. Does not handle authentication or key exchange. 
**Example:** 
- SSL/TLS Protocol: TLS 1.3 encrypts web traffic (HTTPS) between browsers and servers. 
- Encryption Algorithm: AES/XOR encrypts a file, but it doesn't manage communication or authentication.
### SSL Certificate Formats
An **SSL certificate** is a cryptographic file adhering to the X.509 standard. It secures web communication by authenticating a website's identity and enabling encrypted data transfer via the SSL/TLS protocol.
### Certificate Structure
- Defined in **ASN.1 notation**.
- **Encoding Scheme**:  
  - Binary
  - Base64
### Common Formats & File Extensions
#### Base64-Encoded (Text-Based)
- **PEM**  
  - Extensions: `.pem`, `.crt`, `.key`, `.cer`
- **PKCS#7**  
  - Extensions: `.p7c`, `p7c`
#### Binary-Encoded
- **DER**  
  - Extensions: `.der`, `.cer`  
- **PKCS#12**  
  - Extensions: `.pfx`, `.p12`  
### Diagram Overview

```mermaid
graph TD
  %% Define encoding schemes
  SSL -->|Encoding Scheme| Base64
  SSL -->|Encoding Scheme| Binary

  %% Base64 branch
  Base64 --> PEM
  PEM -->|File Extensions| .pem
  PEM -->|File Extensions| .key
  PEM -->|File Extensions| .crt
  PEM -->|File Extensions| .cer

  Base64 --> PKCS7
  PKCS7 -->|File Extensions| .p7b
  PKCS7 -->|File Extensions| .p7c

  %% Binary branch
  Binary --> DER
  DER -->|File Extensions| .der
  DER -->|File Extensions| .cer

  Binary --> PKCS12
  PKCS12 -->|File Extensions| .pfx
  PKCS12 -->|File Extensions| .p12
  ```
