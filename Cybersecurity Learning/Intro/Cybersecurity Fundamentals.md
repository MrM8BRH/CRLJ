Systems at Risk
---------------
The growth in the number of computer systems and the increasing reliance upon them by individuals, businesses, industries, and governments means that there are an increasing number of systems at risk.
*   Financial systems
*   Utilities and industrial equipment
*   Aviation
*   Consumer devices
*   Healthcare
*   Large corporations
*   Automobiles
*   Shipping
*   Government
*   Internet of things and physical vulnerabilities
*   Medical systems
*   Energy sector
*   Telecommunications

Foundations of Cybersecurity
----------------------------
1.  **Asset**: Something valuable or important.
2.  **Vulnerability**: Weakness or flaw that can be exploited.
3.  **Threat**: Potential danger or harm.
4.  **Risk**: Chance of loss or harm.
5.  **Countermeasure**: Action taken to reduce risk or mitigate threat.
6.  **Likelihood**: A measure that assesses how likely a threat can exploit one or more vulnerabilities.

* * *

### Classification Roles
1.  **Owner**: Responsible for determining the value and importance of the asset.
2.  **Custodian**: In charge of safeguarding and maintaining the asset.
3.  **User**: Interacts with and utilizes the asset.

* * *

### Classification Criteria
1.  **Value**: Assessing the worth or significance of the asset.
2.  **Age**: Determining how long the asset has been in use.
3.  **Replacement Cost**: Evaluating the expense of acquiring a new asset.
4.  **Useful Life Time**: Estimating how much longer the asset will remain functional.

* * *

### Classifying Vulnerabilities
1.  **Policy Flaws**: Weaknesses in security policies or procedures.
2.  **Design Errors**: Mistakes in the system's architectural plan.
3.  **Protocol Weaknesses**: Vulnerabilities in communication protocols.
4.  **Misconfiguration**: Improperly configured settings or permissions.
5.  **Software Vulnerability**: Weaknesses in software code or applications.
6.  **Human Factor**: Human actions or behaviors that introduce risk.
7.  **Malicious Software**: Harmful programs like viruses or malware.
8.  **Hardware Vulnerability**: Weaknesses in physical components.
9.  **Physical Access to Network Resource**: Unauthorized physical access.
10.  **Natural Factors (fire/earthquake/flood/storms)**: Environmental risks.

* * *

### Classifying Countermeasures
1.  **Administrative**: Policies, procedures, and training to manage security.
2.  **Physical**: Physical safeguards like locks, fences, and surveillance.
3.  **Logical**: Digital measures such as firewalls, encryption, and access controls.

* * *

### CIA Triad
*   **Confidentiality** refers to the protection of sensitive information from unauthorized access, disclosure, or use. This can be achieved through measures such as encryption, access control, and data classification.
    **– \[Encryption | Least Privilege | Access Control\]**
*   **Integrity** refers to the protection of information from unauthorized modification or deletion. This can be achieved through measures such as data validation, version control, and auditing.
    **– \[Hashing | Digital Signature\]**
*   **Availability** refers to the assurance that information and information systems are available when needed. This can be achieved through measures such as redundancy, backup and recovery, and disaster recovery planning.
    **– \[Backup | Remote Sites\]**

* * *

### AAA
**AAA**, which stands for Authentication, Authorization, and Accounting, is a fundamental concept in information security and network management. It is often compared to the CIA triad, which focuses on protecting information, while AAA is more concerned with controlling access to resources and tracking user activities. Let's break down AAA in a similar format to the CIA Triad:
*   **Authentication**: Authentication is the process of verifying the identity of a user, system, or entity. It ensures that the person or system trying to access a resource is who they claim to be. This is typically achieved through mechanisms like passwords, biometrics, smart cards, or other authentication methods.
    **– \[Passwords | Biometrics | Two-factor Authentication\]**
*   **Authorization**: Authorization follows authentication and determines what actions or resources a user or system is allowed to access. It establishes the level of access privileges granted to an authenticated entity. This is often managed through access control lists (ACLs) or role-based access control (RBAC) policies.
    **– \[Access Control Lists | Role-based Access Control\]**
*   **Accounting**: Accounting involves keeping track of activities and events related to the use of resources. It includes logging information such as who accessed what, when, and for how long. This information is crucial for monitoring and auditing purposes, as well as for billing or compliance requirements.
    **– \[Logging | Auditing | Monitoring\]**

* * *

### Supply Chain Risk Management
*   **Prevention**: Implementing measures to prevent risks from occurring.
*   **Preparedness**: Preparing for potential risks by developing contingency plans.
*   **Response**: Taking immediate action when a risk materializes.
*   **Recovery**: Restoring normal operations after a disruption.

* * *

### Risk Management Decisions
*   **Accept**: Acknowledge and document the risk as within tolerance.
*   **Mitigate**: Apply additional controls or improve existing ones
*   **Transfer**: Shift the risk to a third party (e.g., insurance).
*   **Avoid**: Cease the activity or process creating the risk (if feasible).


* * *

### Security Standards and Vulnerability References
- **RFC — Request for Comments:** Technical documents that define Internet protocols, standards, procedures, and best practices. Examples include RFC 791 for IPv4, RFC 8200 for IPv6, and RFC 8446 for TLS 1.3.
- **CWE — Common Weakness Enumeration:** A classification system for common software and hardware weaknesses that may lead to vulnerabilities. Examples include CWE-79 for Cross-Site Scripting and CWE-89 for SQL Injection.
- **CVE — Common Vulnerabilities and Exposures:** A standardized identification system for publicly disclosed security vulnerabilities. Each vulnerability receives a unique identifier, such as `CVE-2021-44228`.

**Relationship**
- An RFC describes how a protocol or technology should operate.
- A CWE describes a general category of security weakness.
- A CVE identifies a specific vulnerability in a particular product or im

* * *

### Threat Modeling Methods
1. STRIDE
2. PASTA
3. DREAD
4. TRIKE
5. VAST
6. Attack Trees
7. OCTAVE
8. QTMM
9. LINDDUN
10. CVSS
11. MITRE ATT&CK
12. Cyber Kill Chain
13. OWASP
14. NIST SP 800-30

* * * 

### Essentials of Cybersecurity Domains

**⌗ Network and Infrastructure Security ⌗**

Protects enterprise networks, communications, and infrastructure from unauthorized access, disruption, lateral movement, and denial-of-service attacks.

Key capabilities include:

* Firewalls and secure web gateways
* Network detection and response
* Intrusion detection and prevention systems
* Network segmentation and microsegmentation
* Virtual private networks and secure access service edge
* Domain Name System security
* Distributed denial-of-service protection
* Network access control
* Secure wireless, 5G, and remote-access infrastructure

Modern network security increasingly follows zero-trust principles, where access is not automatically trusted based on network location. Users, devices, workloads, and requests must be continuously verified.

**⌗ Endpoint and System Security ⌗**

Protects servers, workstations, mobile devices, virtual machines, containers, and other computing platforms from compromise, misuse, malware, and unauthorized access.

Key capabilities include:

* Secure system configuration and hardening
* Patch and vulnerability management
* Endpoint detection and response
* Extended detection and response
* Anti-malware controls
* Host-based firewalls
* Device encryption
* Mobile device management
* Privileged access controls
* Secure boot and hardware-backed security
* Asset inventory and configuration management

The domain also includes platform security for cloud workloads, containers, orchestration platforms, and virtualized environments.

**⌗ Identity and Access Security ⌗**

Ensures that the correct users, devices, applications, and workloads receive appropriate access to resources.

Key practices include:

* Identity and access management
* Multi-factor authentication
* Single sign-on and federation
* Role- and attribute-based access control
* Privileged access management
* Identity governance and administration
* Machine and workload identity management
* Conditional and risk-based access
* Passwordless authentication
* Continuous authentication and authorization
* Joiner, mover, and leaver lifecycle controls

Identity is now a primary security control plane because users and services routinely access resources distributed across on-premises, cloud, software-as-a-service, and partner environments.

**⌗ Application and API Security ⌗**

Protects software, application programming interfaces, web applications, mobile applications, and software services throughout their lifecycle.

Key practices include:

* Secure software development lifecycle
* Threat modeling
* Secure coding
* Input validation and output encoding
* Authentication and authorization testing
* API security
* Software composition analysis
* Static and dynamic application security testing
* Interactive application security testing
* Secrets management
* Runtime application protection
* Penetration testing
* Vulnerability disclosure and remediation

Security should be built into product design and development rather than added after deployment. This reflects the secure-by-design and secure-by-default approach promoted across the software industry.

**⌗ Cloud and Cloud-Native Security ⌗**

Protects infrastructure, platforms, applications, identities, and data hosted in public, private, hybrid, and multi-cloud environments.

Key capabilities include:

* Cloud security posture management
* Cloud-native application protection platforms
* Cloud workload protection
* Cloud infrastructure entitlement management
* Container and Kubernetes security
* Infrastructure-as-code scanning
* Secure cloud configuration
* SaaS security posture management
* Cloud logging and monitoring
* Workload identity
* Multi-cloud governance
* Shared-responsibility management

Cloud security must address configuration errors, excessive permissions, exposed services, insecure APIs, vulnerable workloads, and inconsistent controls across multiple providers.

**⌗ Data Security and Privacy ⌗**

Protects information throughout its lifecycle, including collection, creation, storage, processing, transmission, sharing, archival, and destruction.

Key practices include:

* Data discovery and classification
* Encryption at rest and in transit
* Key and certificate management
* Data loss prevention
* Database security
* Tokenization and masking
* Rights management
* Secure backup and recovery
* Data retention and deletion
* Privacy engineering
* Access monitoring
* Data security posture management

Organizations should also maintain cryptographic inventories and migration plans for post-quantum cryptography. NIST’s first finalized post-quantum standards are available for implementation, making cryptographic agility and transition planning an operational requirement.

**⌗ Security Operations and Threat Management ⌗**

Detects, investigates, contains, and responds to malicious activity across the organization.

Key capabilities include:

* Security information and event management
* Security orchestration, automation, and response
* Endpoint, network, identity, and cloud detection
* Threat intelligence
* Threat hunting
* Detection engineering
* Malware analysis
* Digital forensics
* User and entity behavior analytics
* Continuous monitoring
* Security operations center processes
* Exposure and attack-surface management

Effective security operations require high-quality telemetry, tested detection logic, documented escalation paths, and measurable response processes.

**⌗ Incident Response, Resilience, and Recovery ⌗**

Prepares the organization to manage security incidents, limit operational impact, restore services, and learn from events.

Key practices include:

* Incident response planning
* Defined roles and escalation procedures
* Incident classification and prioritization
* Containment, eradication, and recovery
* Crisis communications
* Digital forensics
* Ransomware response
* Business continuity
* Disaster recovery
* Immutable and offline backups
* Tabletop exercises
* Post-incident reviews
* Lessons-learned tracking

Resilience extends beyond preventing attacks. It includes maintaining critical operations and recovering within acceptable business timeframes.

**⌗ Vulnerability and Exposure Management ⌗**

Identifies, assesses, prioritizes, and remediates weaknesses across internal systems, internet-facing assets, applications, cloud environments, and third-party services.

Key capabilities include:

* Vulnerability scanning
* Asset and attack-surface discovery
* Risk-based vulnerability prioritization
* Penetration testing
* Red-team and purple-team exercises
* Configuration assessment
* Patch management
* Breach and attack simulation
* Continuous control validation
* External attack-surface management
* Remediation verification

Prioritization should consider exploitability, asset criticality, exposure, active threat activity, control effectiveness, and potential business impact—not severity scores alone.

**⌗ Governance, Risk, and Compliance ⌗**

Establishes organizational direction, accountability, oversight, and risk-management processes for cybersecurity.

Key activities include:

* Cybersecurity strategy
* Governance structures and accountability
* Risk assessment and treatment
* Security policies and standards
* Regulatory and contractual compliance
* Control design and assurance
* Cybersecurity metrics and reporting
* Budget and resource prioritization
* Security awareness and role-based training
* Third-party risk governance
* Exception and risk-acceptance processes
* Board and executive reporting
* Cyber insurance coordination

Governance should align cybersecurity decisions with business objectives, legal obligations, operational dependencies, and enterprise risk appetite.

**⌗ Third-Party and Software Supply-Chain Security ⌗**

Manages risks introduced by suppliers, contractors, software vendors, open-source components, cloud providers, and other external dependencies.

Key practices include:

* Supplier security assessments
* Contractual security requirements
* Software bills of materials
* Dependency and component analysis
* Code-signing and artifact integrity
* Vendor access controls
* Continuous third-party monitoring
* Concentration-risk assessment
* Secure procurement
* Supply-chain incident response
* Open-source software governance
* End-of-life and product-support monitoring

Supply-chain security should cover both organizational vendors and the components, build systems, repositories, dependencies, and services used to produce software.

**⌗ Operational Technology, IoT, and Cyber-Physical Security ⌗**

Protects industrial control systems, operational technology, Internet of Things devices, building systems, medical devices, and other cyber-physical environments.

Key practices include:

* OT and IoT asset discovery
* Network segmentation
* Secure remote access
* Protocol-aware monitoring
* Safety and availability protection
* Firmware and device integrity
* Compensating controls for legacy systems
* Vendor access governance
* Secure configuration
* Incident response adapted to operational environments
* Physical and cybersecurity coordination

Controls must account for safety, reliability, deterministic operations, long equipment lifecycles, and systems that cannot be patched or interrupted using standard IT procedures.

**⌗ AI and Machine-Learning Security ⌗**

Protects artificial intelligence systems and manages security risks created by organizational use of generative AI and machine-learning technologies.

Key areas include:

* AI asset and model inventory
* Training-data protection
* Prompt-injection defenses
* Model and data access controls
* Sensitive-data leakage prevention
* Adversarial testing
* Model supply-chain security
* Output validation
* AI-generated code review
* Agent and tool permission controls
* Monitoring for model misuse
* Human oversight
* AI incident response
* Governance of approved and prohibited use cases

AI security should address both securing AI systems and using AI safely within conventional business and security processes.

**⌗ Security Architecture and Engineering ⌗**

Designs and maintains security controls as an integrated part of enterprise technology architecture.

Key practices include:

* Zero-trust architecture
* Defense in depth
* Secure reference architectures
* Threat modeling
* Security design reviews
* Cryptographic architecture
* Segmentation and isolation
* Resilience engineering
* Secure configuration baselines
* Architecture exception management
* Control integration and validation
* Technology lifecycle planning

Security architecture connects individual security tools and controls into a coherent system aligned with business and operational requirements.

* * *

### Exploring Cybersecurity Teams
**Blue Team:**
*   The defensive force ensuring and enhancing an organization's security.
*   Comprising security professionals dedicated to risk identification, incident response, and policy compliance.

**Red Team:**
*   The offensive unit simulating real-world attacks to assess security vulnerabilities.
*   Comprising skilled professionals using attacker techniques to uncover weaknesses in an organization's defenses.

**Purple Team:**
*   A collaborative force merging Blue and Red Teams for enhanced security.
*   Involves joint efforts to identify, address, and strengthen security measures by leveraging the strengths of both defensive and offensive teams.

<div align="center">

<img width="800" height="800" alt="image" src="https://github.com/user-attachments/assets/1893a3e6-02b9-47d4-b4b7-6b34e5eb3e94" />
<img width="1024" height="1535" alt="image" src="https://github.com/user-attachments/assets/5732ea4e-27f3-4647-8357-c766f09f7c32" />

![image](https://github.com/user-attachments/assets/a509c7a2-ee6c-408f-b487-773298d027cd)
![image](https://github.com/user-attachments/assets/9dcf458b-8b73-43f8-af0e-023d2d4cf308)
<img src="https://github.com/user-attachments/assets/334331ef-f81a-4402-860f-08d598ab742c" width="350px" hight="250px">
<img width="800" height="533" alt="image" src="https://github.com/user-attachments/assets/bce2e52f-4191-47e7-b0e4-f3c470cff2b6" />
<br>
<img src="https://github.com/MrM8BRH/MrM8BRH/assets/34133187/3f46d342-6aab-4d00-b3ef-968ae825ae7e" width="550px" hight="350px">
![thesecmap](https://github.com/user-attachments/assets/588b9ac3-97fc-4118-b264-704815957c22)
![teams](https://github.com/MrM8BRH/MrM8BRH/assets/34133187/189b9dd5-c394-4101-a7f6-032d1f97955a)
![Red-Purple-and-Blue-Team-Exercises](https://github.com/MrM8BRH/MrM8BRH/assets/34133187/ce8dc507-3d3c-4747-9d6b-c3cab12852cb)
![DS](https://github.com/MrM8BRH/MrM8BRH/assets/34133187/1489cebc-5dd1-4e7b-b49a-03c7b086e61e)
![DL](https://github.com/MrM8BRH/MrM8BRH/assets/34133187/b4c6605b-af2b-4673-b703-2a855f9a5b5f)
![POP](https://github.com/user-attachments/assets/4c27766b-d7bd-4f42-8a00-52878dbdbb07)
![DII](https://github.com/user-attachments/assets/5ef0e286-f610-42ed-9797-560ffd4d8e49)
  
</div>
