Digital Forensics and Incident Response (DFIR)
----------------------------------------------
DFIR integrates two discrete cybersecurity disciplines: Digital forensics, the investigation of cyberthreats, primarily to gather digital evidence for litigating cybercriminals; and incident response, the detection and mitigation of cyberattacks in progress. By combining these two disciplines, DFIR helps security teams stop threats faster, while preserving evidence that might otherwise be lost in the urgency of threat mitigation.

Digital Forensics (DF)
----------------------
Digital forensics investigates and reconstructs cybersecurity incidents by collecting, analyzing, and preserving digital evidence—traces left behind by threat actors, such as malware files and malicious scripts. These reconstructions allow investigators to pinpoint the root causes of attacks and identify the culprits. 

Digital forensic investigations follow a strict chain of custody, or formal process for tracking how evidence is gathered and handled. The chain of custody allows investigators to prove evidence hasn’t been tampered with. As a result, evidence from digital forensics investigations can be used for official purposes like court cases, insurance claims, and regulatory audits.

[The National Institute of Standards and Technology (NIST)](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-86.pdf) outlines four steps for digital forensic investigations:
1. Data collection

After a breach, forensic investigators collect data from operating systems, user accounts, mobile devices, and any other hardware and software assets threat actors may have accessed. Common sources of forensic data include:
- File system forensics: Data found in files and folders stored on endpoints. 
- Memory forensics: Data found in a device’s random access memory (RAM).
- Network forensics: Data found by examining network activity like web browsing and communications between devices. 
- Application forensics: Data found in the logs of apps and other software. 

To preserve evidence integrity, investigators make copies of data before processing it. They secure the originals so they cannot be altered, and the rest of the investigation is carried out on the copies.

2. Examination
Investigators comb through the data for signs of cybercriminal activity, such as phishing emails, altered files, and suspicious connections.

3. Analysis
Investigators use forensic techniques to process, correlate, and extract insights from digital evidence. Investigators may also reference proprietary and open-source threat intelligence feeds to link their findings to specific threat actors.

4. Reporting
Investigators compile a report that explains what happened during the security event and, if possible, identifies suspects or culprits. The report may contain recommendations for thwarting future attacks. It can be shared with law enforcement, insurers, regulators, and other authorities.

What is Incident Response (IR)?
--------------------------
Incident response (sometimes called cybersecurity incident response) refers to an organization’s processes and technologies for detecting and responding to cyberthreats, security breaches or cyberattacks. The goal of incident response is to prevent cyberattacks before they happen, and to minimize the cost and business disruption resulting from any cyberattacks that occur.

Ideally, an organization defines incident response processes and technologies in a formal incident response plan (IRP) that specifies exactly how different types of cyberattacks should be identified, contained, and resolved. An effective incident response plan can help cybersecurity teams detect and contain cyberthreats and restore affected systems faster, and reduce the lost revenue, regulatory fines and other costs associate with these threats.

Incident Response Phases:
-------------------------
#### Phase I – Preparation

The major steps of this phase are as follows:

*   Identification of the most important assets and protecting them with all your efforts, and
*   Analysis of data collected from earlier incidents

#### Phase II – Identification
Usually, an incident falls under six classifications:
1.  Unauthorized access
2.  Denial of services
3.  Malicious code
4.  Improper usage
5.  Scans/probes/attempted access
6.  Investigation incident

#### Phase III – Containment
Having gathered all the necessary information about the incident, the IR team should now be concentrating on the containment of the threat for preventing any further damage. The first step of this phase should be to isolate the infected machine from the network and to back up all the sensitive data of the infected system.

After this, you can go for a temporary fix to ensure that the incident won’t escalate its damage anymore. The primary goal of this phase is to minimize the scope and magnitude of the incident. Make sure you gauge the functional status of your infected system or network. To determine this, you can opt for any of the listed options:

**Option 1:** Disconnect the infected entity and let it continue with its standalone operations.

**Option 2:** Shut down the whole system immediately.

**Option 3:** Let the system operate as usual and keep monitoring its activities.

The detailed log for evidence should contain:
*   **Evidence identifying information:** Serial number, model number, hostname, MAC and IP addresses, and location
*   **Evidence holder’s Information:** Name, title, and phone number
*   **Location, time, and date with time zone:** For each occurrence of evidence handling

#### Phase IV – Eradication
Eradication is a simple process of eliminating the threat out of your infected network or system. This phase should only start when all the other internal and external actions are completed. The two important aspects of this phase are as follows:

**Clean-up:** The process of clean-up should include running a powerful antimalware and antivirus software, uninstalling the infected software, rebooting or replacing the entire operating system and hardware (based on the scope of the incident), and rebuilding the network.

**Notification:** Notify all the personnel involved, according to the reporting chain.

It is advisable to create multiple common incident “playbooks” that can help the IR team to take a consistent approach to the incident.

#### Phase V – Recovery

At this stage, the compromised system or network will be brought back to life. From the data recovery to any remaining restoration process, this phase covers it all. It takes place in two steps:

**Service restoration:** As per the corporate contingency plans.  
**System/network validation:** Testing and verifying the system/network in a functional state.

This phase makes sure that the infected entity is recertified as both secure and functional.

#### Phase VI – Lessons Learned

After the completion of the investigation, maintain detailed documentation of the complete incident. This last stage will keep your organization prepared for any future attacks and help you to gain value from incidents.

Incident Response Resources and Playbooks
-----------------------------------------
- [Windows Incident Response](https://windowsir.blogspot.com/)
- [Incident Response Playbooks](https://www.incidentresponse.org/playbooks/)
- [SANS Incident Handling Policy Templates](https://www.sans.org/information-security-policy/?category=incident-handling)
- [Atomic Threat Coverage](https://atc-project.github.io/atc-react/)
- [Fucking Awesome Incident Response](https://github.com/Correia-jpv/fucking-awesome-incident-response)
- [Awesome Incident Response](https://github.com/meirwah/awesome-incident-response)
- [Applied Incident Response Resources](https://www.appliedincidentresponse.com/resources/)
- [Incident Playbook](https://github.com/austinsonger/Incident-Playbook)
- [MISP Playbooks](https://github.com/MISP/misp-playbooks)
- [SOCFortress Playbooks](https://github.com/socfortress/Playbooks)
- [CaseManager](https://github.com/crowdere/CaseManager)
- [Incident Response Linux](https://github.com/vm32/Linux-Incident-Response)
- [ID Ransomware](https://id-ransomware.malwarehunterteam.com/)
- [No more Ransom](https://www.nomoreransom.org/en/index.html)

Cheat Sheets, OSs and Tools
----
- [DFIR Cheat Sheet](https://dfircheatsheet.github.io/)
- [Introduction to DFIR](https://a1l4m.medium.com/introduction-to-dfir-290d77c60965)
- [Forensics Start Page](https://start.me/p/q6mw4Q/forensics)
- [Free hands-on digital forensics labs for students and faculty](https://github.com/frankwxu/digital-forensics-lab)
- [Digital Forensics Script for Linux](https://github.com/vm32/Digital-Forensics-Script-for-Linux)
- [FREE DFIR First Responder Bootcamp](https://www.poppopret.training/free-dfir-first-responder-bootcamp)
- [Awesome Forensics](https://github.com/cugu/awesome-forensics)
- [Collection of forensic tools](https://github.com/cristianzsh/forensictools)
- [Awesome Memory Forensics](https://github.com/digitalisx/awesome-memory-forensics)
- [Image OSINT Forensics](https://github.com/CScorza/Image-OSINT-Forensics)
- [DFIR Training](https://www.dfir.training/)
- [Epoch Converter](https://www.epochconverter.com/)
- [DFIR cheatsheet](https://www.jaiminton.com/cheatsheet/DFIR/#)
- [CSI Linux](https://csilinux.com/)
- [CSI Linux Certified Investigator Course](https://csilinux.com/courses/csi-linux-certified-investigator/)
- [CAINE (Computer Aided INvestigative Environment)](https://www.caine-live.net/)
- [Paladin](https://sumuri.com/software/paladin/)
- [The Sleuth Kit](https://sleuthkit.org/)
- [NirSoft](https://www.nirsoft.net/)
- [Forensic Magnifier](https://29a.ch/photo-forensics/#forensic-magnifier)
- [OSForensics](https://www.osforensics.com/download.html)
- [OSForensics Official Website](https://www.osforensics.com/index.html)
- [SalvationDATA Database Forensic Analysis System](https://www.salvationdata.com/business-list-page/database-forensic-analysis-system/)
- [Forensic Analysis Workstation (FAW)](https://en.fawproject.com/)
- [Registry Spy](https://github.com/andyjsmith/Registry-Spy)
- [Wielview](https://github.com/williamskosasi/Wielview)
- [SOC Multitool](https://github.com/zdhenard42/SOC-Multitool)
- [LogonTracer](https://github.com/JPCERTCC/LogonTracer)
- [PWF](https://github.com/bluecapesecurity/PWF)
- [Sn1per](https://github.com/1N3/Sn1per)
- [Malware](https://github.com/rivitna/Malware)
- [Forensics Start Page](https://start.me/p/q6mw4Q/forensics)
- [Velociraptor](https://github.com/Velocidex/velociraptor)
- [Autopsy](https://www.sleuthkit.org/autopsy/)
- [Encrypted Disk Detector](https://www.magnetforensics.com/resources/encrypted-disk-detector/)
- [Magnet RAM Capture](https://www.magnetforensics.com/resources/magnet-ram-capture/)
- [NetworkMiner](https://www.netresec.com/?page=NetworkMiner)
- [RAM Capturer](https://belkasoft.com/ram-capturer)
- [FAW Project](https://en.fawproject.com/download/)
- [HashMyFile](https://www.nirsoft.net/utils/hash_my_files.html)
- [CrowdStrike Community Tools](https://www.crowdstrike.com/resources/community-tools/)
- [Defraser (Detect Multimedia Files)](https://sourceforge.net/projects/defraser/)
- [Toolsley - Toolbox](https://www.toolsley.com/)
- [SIFT Workstation](https://www.sans.org/tools/sift-workstation/)
- [Dumpzilla (Browser Info Extractor)](https://www.dumpzilla.org/)
- [Browser History Viewer](https://www.foxtonforensics.com/browser-history-viewer/)
- [ForensicUserInfo](https://github.com/woanware)
- [PALADIN Forensic Suite](https://sumuri.com/software/paladin/)
- [The Sleuth Kit](https://www.sleuthkit.org/sleuthkit/)
- [CAINE (Computer Aided Investigate Environment)](https://www.caine-live.net/)
- [Volatility (Memory Forensics Framework)](https://www.volatilityfoundation.org/)
- [WindowSCOPE Cyber Forensics](https://www.windowsscope.com/windowsscope-cyber-forensics/)
- [TCT (Unix System Analysis)](http://www.porcupine.org/forensics/tct.html)
- [Bulk Extractor (Extract Useful Information)](https://downloads.digitalcorpora.org/downloads/bulk_extractor/)
- [Oxygen Forensic Suite](https://www.oxygen-forensic.com/en/products/oxygen-forensic-kit)
- [Xplico (Network Forensic Analysis Tool)](https://www.xplico.org/download)
- [AES Finder](https://github.com/mmozeiko/aes-finder)
- [inVtero.net](https://github.com/ShaneK2/inVtero.net)
- [Muninn](https://github.com/ytisf/muninn) 
- [Rekall](http://www.rekall-forensic.com/)
- [AChoir](https://github.com/OMENScan/AChoir)
- [python-evt](https://github.com/williballenthin/python-evt)
- [python-registry](http://www.williballenthin.com/registry/)
- [RegRipper](https://github.com/keydet89/RegRipper4.0)
- [WDBGARK](https://github.com/swwwolf/wdbgark)

Ransomware Decryption Tool
--------------------------
- [Quick Heal Ransomware Decryption Tool](https://www.quickheal.com/free-ransomware-decryption-tool/)
- [No More Ransom](https://www.nomoreransom.org/en/decryption-tools.html)
- [Emsisoft Ransomware Decryption Tools](https://www.emsisoft.com/en/ransomware-decryption/)
- [Kaspersky No Ransom](https://noransom.kaspersky.com/)
- [Avast Ransomware Decryption Tools](https://www.avast.com/ransomware-decryption-tools#pc)
- [BugsFighter Ransomware Decryption Tools](https://www.bugsfighter.com/ransomware/)
- [BleepingComputer Ransomware Decryptors](https://www.bleepingcomputer.com/download/windows/ransomware-decryptors/)

<div align="center">

<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/c3e76b16-e890-42d6-ac74-cbbbd52ac4c6" />

![Hierarchy-DFIR](https://github.com/MrM8BRH/MrM8BRH/assets/34133187/2d11688b-ddcb-41a3-9308-c5880e8ab385)
![IR](https://github.com/MrM8BRH/MrM8BRH/assets/34133187/29944e79-f81f-40d7-884b-6120b0fe49a7)

<img width="998" height="999" alt="image" src="https://github.com/user-attachments/assets/d45b45ff-2bfa-4aae-b163-a4cb15e2e0af" />
<img width="800" height="1200" alt="image" src="https://github.com/user-attachments/assets/0990a393-6947-46b1-ba91-55b87c677404" />
<img width="1168" height="1636" alt="image" src="https://github.com/user-attachments/assets/5b330226-2c6c-4cbf-914a-86868fd819d2" />
<img width="800" height="533" alt="image" src="https://github.com/user-attachments/assets/f2f631af-9dde-4d8b-af89-fac2af897eba" />

</div>
