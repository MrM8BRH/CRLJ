Active Directory Penetration Testing
------------------------------------
 Active Directory penetration testing is a proactive approach to discover potential vulnerabilities in an AD environment. By simulating cyber-attacks in a controlled setting, organizations can identify weak points and rectify them before malicious actors exploit them.

Key Areas to Focus On:

- **Pre-Engagement Interaction:** Understand the scope of the test.Establish communication protocols.Ensure necessary permissions are in place.
- **Information Gathering:** Enumerate domain information.Extract user details, group memberships, and trusts.Identify domain controllers and their roles.
- **Enumeration:** Utilize tools like PowerView and BloodHound to gather detailed AD data.Enumerate sessions, shares, and group policies.
- **Credential Assessment:** Extract NTLM hashes and Kerberos tickets.Perform pass-the-hash or pass-the-ticket attacks.Use tools like Mimikatz for credential dumping.
- **Lateral Movement:** Exploit weak service configurations.Utilize tools like CrackMapExec and PowerUpSQL for lateral traversal.
- **Privilege Escalation:** Identify misconfigurations using tools like PowerUp.Exploit Kerberos vulnerabilities, such as Kerberoasting.
- **Domain Dominance:** Extract the NTDS.dit file for offline extraction.Create a Golden Ticket using Kerberos Ticket Granting Ticket (TGT).
- **Data Exfiltration:** Identify sensitive data.Use tools like Rclone or SMB to transfer data securely.
- **Post Exploitation:** Maintain persistence using tools like Empire or Metasploit.Deploy backdoors and monitor for ongoing access.
- **Reporting:**
  - Document findings, methodologies, and tools used.
  - Provide a detailed risk assessment.
  - Offer actionable recommendations to bolster security.

Resources and Tools
-------------------
- [OCD Mind Maps](https://orange-cyberdefense.github.io/ocd-mindmaps/)
- [OWASP Offensive Active Directory 101 (PDF)](https://owasp.org/www-pdf-archive/OWASP_FFM_41_OffensiveActiveDirectory_101_MichaelRitter.pdf)
- [AD Attack-Defense by infosecn1nja](https://github.com/infosecn1nja/AD-Attack-Defense)
- [Vulnerable AD Lab](https://shellcode.blog/Vulnerable-AD-Lab-IaC/)
- [LinWinPwn](https://github.com/lefayjey/linWinPwn)
- [Attacking Active Directory](https://zer1t0.gitlab.io/posts/attacking_ad/)
- [ADSecurity](https://adsecurity.org/)
- [Dirk-Jan's Blog](https://dirkjanm.io/)
- [Lateral Movement Megaprimer](https://riccardoancarani.github.io/2019-10-04-lateral-movement-megaprimer/)
- [Windows Red Team Lateral Movement Techniques](https://www.linode.com/docs/guides/windows-red-team-lateral-movement-techniques/)
- [Red Teaming Lateral Movement Techniques](https://klezvirus.github.io/RedTeaming/LateralMovement/)
- [Operator-UP: Windows Lateral Movement Techniques](https://obscuritylabs.github.io/operator-up/windows/lat_movement/)
- [SMB Psexec, SMBExec, Winexe - How To](https://nv2lt.github.io/windows/smb-psexec-smbexec-winexe-how-to/)
- [Offensive Lateral Movement Techniques](https://eaneatfruit.github.io/2019/08/18/Offensive-Lateral-Movement/)
- [ldapnomnom](https://github.com/lkarlslund/ldapnomnom)
- [PingCastle - Active Directory Security Assessment](https://www.pingcastle.com/)
- [Forensia](https://github.com/PaulNorman01/Forensia)
- [Windows Notes and Cheatsheet](https://m0chan.github.io/2019/07/30/Windows-Notes-and-Cheatsheet.html)
- [Wadcoms](https://wadcoms.github.io/)
- [Useful Random Stuff](https://github.com/purpl3f0xsecur1ty/useful_random_stuff)
- [Impacket](https://www.secureauth.com/labs-old/impacket/)
- [Internal-Monologue](https://github.com/eladshamir/Internal-Monologue)
- [Windows Active Directory Exploitation Cheat Sheet and Command Reference](https://casvancooten.com/posts/2020/11/windows-active-directory-exploitation-cheat-sheet-and-command-reference/)
- [Win32 Offensive Cheatsheet](https://github.com/matthieu-hackwitharts/Win32_Offensive_Cheatsheet)
- [Active Directory Exploitation Cheat Sheet](https://github.com/S1ckB0y1337/Active-Directory-Exploitation-Cheat-Sheet)
- [Purple Knight Resources](https://www.purple-knight.com/resources/)
- [PingCastle](https://www.pingcastle.com/)
- [HardeningKitty](https://github.com/scipag/HardeningKitty)
- [SecureAD](https://github.com/LoicVeirman/SecureAD)
- [WADComs](https://wadcoms.github.io/)
- [Windows Notes and Cheatsheet](https://m0chan.github.io/2019/07/30/Windows-Notes-and-Cheatsheet.html)
- [The Hacker Recipes - AD Recon](https://www.thehacker.recipes/ad/recon)
- [AD Pentesting Tools](https://github.com/theyoge/AD-Pentesting-Tools)
- [Responder](https://github.com/lgandx/Responder)
- [BloodHound](https://github.com/BloodHoundAD/BloodHound)
- [Mimikatz](https://blog.gentilkiwi.com/mimikatz)
- [CrackMapExec](https://github.com/byt3bl33d3r/CrackMapExec)
- [linWinPwn](https://github.com/lefayjey/linWinPwn)
- [msLDAPDump](https://github.com/dievus/msLDAPDump)
- [LDAP Nom Nom](https://github.com/lkarlslund/ldapnomnom)
- [Coercer](https://github.com/p0dalirius/Coercer)
- [Impacket](https://github.com/fortra/impacket)
- [lsassy](https://github.com/Hackndo/lsassy)
- [Ridrelay](https://github.com/skorov/ridrelay)
- [Certipy](https://github.com/ly4k/Certipy)
- [Kubestroyer](https://github.com/Rolix44/Kubestroyer)
- [GOAD](https://github.com/Orange-Cyberdefense/GOAD)
- [vulnerable-AD-plus](https://github.com/WaterExecution/vulnerable-AD-plus)
- [Hardentools](https://github.com/hardentools/hardentools)
- [ForEnergy](https://forsenergy.com/)
- [Windows Security](https://www.windows-security.org/)
- [ADMX](https://admx.help/)
- [Ultimate Windows Security](https://www.ultimatewindowssecurity.com/)
- [Woshub](https://woshub.com/)

## 1. Introduction to Active Directory  
- **Definition**: Centralized directory service for managing Windows-based networks.  
- **Core Functions**:  
  - Stores and organizes network resources (users, devices, policies).  
  - Enforces security policies and authentication.  
  - Facilitates Single Sign-On (SSO) and delegated administration.  
- **Scalability**: Supports millions of objects; used by ~95% of Fortune 500 companies.  
---
## 2. Core Components & Architecture  
### Key Components  
- **AD Domain Services (AD DS)**: Manages domain join, authentication, and resource access.  
- **AD Lightweight Directory Services (AD LDS)**: Lightweight directory for application-specific data.  
- **AD Federation Services (AD FS)**: Enables SSO across organizations.  
- **AD Certificate Services (AD CS)**: Issues and manages digital certificates.  
### Architectural Hierarchy  
- **Forest**: Top-level container; multiple domains with shared schemas.  
- **Tree**: Hierarchical grouping of domains under a forest.  
- **Domain**: Security boundary for objects (users, groups, devices).  
- **Organizational Units (OUs)**: Subdivisions for applying Group Policies.  
- **Sites & Subnets**: Map physical network topology for efficient replication.  
---
## 3. Key AD Objects  
- **Users**: Domain/local accounts with assigned permissions.  
- **Computers**: Devices joined to the domain.  
- **Groups**:  
  - **Scopes**: Domain Local, Global, Universal.  
  - **Types**: Security (permissions), Distribution (email lists).  
- **Shared Folders**: Network-accessible resources.  
- **Domain Controllers (DCs)**: Host AD DS and manage authentication.  
---
## 4. Replication & Trusts  
### Replication  
- Synchronizes data between DCs.  
- **Types**:  
  - **Intra-Site**: Frequent, uncompressed (same physical location).  
  - **Inter-Site**: Scheduled, compressed (cross-site).  
### Trusts  
- Enable cross-domain resource sharing.  
- **Trust Types**:  
  - **Transitive**: Automatically extends to other domains in the forest.  
  - **Non-Transitive**: Restricted to explicitly defined domains.  
- **Example**:  
```plaintext
Forest Trust: wingtiptoys.com ↔ tailspintoys.com
```
## 5. Group Policy Management  
- **Group Policy Objects (GPOs)**: These define security, software, and system configurations for users and computers.  
- **Scope**: GPOs can be applied to Sites, Domains, or Organizational Units (OUs).  
- **Key Use Cases**:  
  - Enforcing firewall and antivirus policies.  
  - Restricting local admin privileges.  
  - Configuring Single Sign-On (SSO) and audit settings.

### Group Policy Management Console (GPMC)  
```plaintext
Forest: adlab.org  
└─ Domains  
   └─ adlab.org  
      ├─ Default Domain Policy  
      ├─ Domain Controllers (Default Domain Controllers Policy)  
      └─ Workstations/Servers (Custom GPOs)
```
## 6. Authentication Protocols (NTLM vs. Kerberos)  
### NTLM (Legacy)  
- **Mechanism**: NTLM uses a challenge-response protocol to authenticate users to network resources.  
- **Weaknesses**: NTLM is susceptible to pass-the-hash attacks, which make it vulnerable to modern security threats. As a result, it is considered outdated and less secure.
### Kerberos (Default)  
- **Workflow**:  
  - **AS_REQ/AS_REP**: The client sends a request to the Key Distribution Center (KDC) for a Ticket Granting Ticket (TGT), which is used to access resources.  
  - **TGS_REQ/TGS_REP**: The client requests a service ticket from the KDC to access a specific service on the network.  
  - **AP_REQ/AP_REP**: The client uses the service ticket to authenticate to the requested service, granting access.  
- **PAC (Privilege Attribute Certificate)**: The PAC is embedded within the Kerberos tickets to verify and enforce the user's permissions during authentication, ensuring secure access control.
---
## 7. Users, Groups, & Computers  
### User Management  
- **Local Users**: These accounts are specific to individual machines and are not centrally managed by Active Directory.  
- **Domain Users**: Managed centrally through Active Directory, domain users can access network resources based on their assigned permissions and group memberships.
### Group Strategies  
- **AGDLP**: This strategy involves nesting global groups within domain local groups for efficient and controlled resource access. Global groups are typically used for permissions, while domain local groups define access to resources.  
- **Least Privilege**: This principle ensures that users and administrators are given the minimum permissions necessary to perform their job functions, reducing the risk of unauthorized access or accidental changes.
---
## 8. Active Directory Certificate Services (ADCS)  
### Components  
- **Certificate Authorities (CAs)**:  
  - **Root CA**: The top-most authority in the Public Key Infrastructure (PKI) hierarchy, trusted by all entities in the network.  
  - **Subordinate CAs**: These issue certificates under the Root CA, extending the PKI's trust chain.  
- **Certificate Templates**: Define the usage of certificates, such as for secure email, VPN access, or smart card logon.
### Best Practices  
- **Treat CAs as Tier 0 assets**: Given their critical role in network security, Certificate Authorities must be protected and secured as top-tier assets within the organization.  
- **Monitor Event IDs**: Keep an eye on specific Event IDs such as 4768 (for certificate enrollment) and 4886 (for CA configuration changes) to detect potential security issues.
---
## 9. Security Hardening Best Practices  
### Protocol Hardening  
- **Disable**:  
  - LLMNR (Link-Local Multicast Name Resolution)  
  - NetBIOS (NBT-NS)  
  - NTLMv1 (an older and insecure version of NTLM)  
- **Enable**:  
  - SMB signing: Ensures that file-sharing communications are authenticated and integrity-checked.  
  - Kerberos AES encryption: Use AES encryption in Kerberos authentication to enhance security and mitigate vulnerabilities.
### Kerberos Hardening  
- **Rotate KRBTGT account password every 180 days**: Regularly changing the KRBTGT (Kerberos Ticket Granting Ticket) password helps mitigate the risk of ticket forgery.  
- **Use Group Managed Service Accounts (GMSA)**: GMSAs provide automated password management for service accounts, reducing the risk of manual errors and enhancing security.
### Password Policies  
- **Minimum Length**: Enforce a minimum password length of 15 characters to enhance password strength and reduce the likelihood of brute force attacks.  
- **Multi-Factor Authentication (MFA)**: For accounts with elevated privileges, enforce MFA to add an additional layer of security beyond just a password.
### ADCS Hardening  
- **Audit certificate template changes**: Keep track of any modifications to certificate templates to prevent unauthorized changes that could impact security.  
- **Restrict HTTP Endpoints**: Limit access to Certificate Authority endpoints by only allowing trusted and authorized IPs to communicate with them.
---
## 10. Troubleshooting & Optimization  
### Tools  
- **Event Viewer**: Use the Event Viewer to monitor and troubleshoot Kerberos-related issues (e.g., Event IDs 4768-4771) and identify replication errors.  
- **Performance Monitor**: This tool helps you monitor replication latency, track GPO processing times, and diagnose any performance issues that could affect Active Directory's efficiency.
### Optimization Tips  
- **DNS Configuration**: Ensure that SRV records are correctly configured in DNS, as these records are crucial for domain controller discovery and replication.  
- **Replication**: Align Active Directory sites and subnets with the physical network topology to optimize replication traffic and reduce latency.  
- **GPOs**: Minimize the use of "Block Inheritance" and "Enforce" settings to avoid conflicts and improve performance when applying Group Policy Objects.
