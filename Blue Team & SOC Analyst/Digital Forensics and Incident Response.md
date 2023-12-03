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

[Incident Response (IR)](https://github.com/MrM8BRH/CRLJ/blob/main/Blue%20Team%20%26%20SOC%20Analyst/Incident%20Response.md)
-----------------------------------------------------------------------------------------------------------------------------------

Cheat Sheets, OSs and Tools
----
- [DFIR Cheat Sheet](https://dfircheatsheet.github.io/)
- [Introduction to DFIR](https://a1l4m.medium.com/introduction-to-dfir-290d77c60965)
- [Forensics Start Page](https://start.me/p/q6mw4Q/forensics)
- [Awesome Forensics](https://github.com/cugu/awesome-forensics)
- [Awesome Memory Forensics](https://github.com/digitalisx/awesome-memory-forensics)
- [Image OSINT Forensics](https://github.com/CScorza/Image-OSINT-Forensics)
- [DFIR Training](https://www.dfir.training/)
- [Epoch Converter](https://www.epochconverter.com/)
- [DFIR cheatsheet](https://www.jaiminton.com/cheatsheet/DFIR/#)
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

![Hierarchy-DFIR](https://github.com/MrM8BRH/MrM8BRH/assets/34133187/2d11688b-ddcb-41a3-9308-c5880e8ab385)

</div>
