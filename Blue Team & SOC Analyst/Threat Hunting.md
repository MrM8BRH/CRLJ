Threat Hunting (TH)
-------------------

**Threat hunting is the practice of proactively searching for cyber threats that are lurking undetected in a network.** Cyber threat hunting digs deep to find malicious actors in your environment that have slipped past your initial endpoint security defenses.

After sneaking in, an attacker can stealthily remain in a network for months as they quietly collect data, look for confidential material, or obtain login credentials that will allow them to move laterally across the environment.

Once an adversary is successful in evading detection and an attack has penetrated an organization’s defenses, many organizations lack the advanced detection capabilities needed to stop the advanced persistent threats from remaining in the network. That’s why threat hunting is an essential component of any defense strategy.

Threat Hunting Methodologies
----------------------------

**Threat hunters assume that adversaries are already in the system**, and they initiate investigation to find unusual behavior that may indicate the presence of malicious activity. In proactive threat hunting, this initiation of investigation typically falls into three main categories:
### Hypothesis-driven investigation
Hypothesis-driven investigations are often triggered by a new threat that’s been identified through a large pool of crowdsourced attack data, giving insights into attackers’ latest tactics, techniques, and procedures (TTP). Once a new TTP has been identified, threat hunters will then look to discover if the attacker’s specific behaviors are found in their own environment.
### Investigation based on known Indicators of Compromise or Indicators of Attack
This approach to threat hunting involves leveraging tactical threat intelligence to catalog known IOCs and IOAs associated with new threats. These then become triggers that threat hunters use to uncover potential hidden attacks or ongoing malicious activity.
### Advanced analytics and machine learning investigations

The third approach combines powerful data analysis and machine learning to sift through a massive amount of information in order to detect irregularities that may suggest potential malicious activity. These anomalies become hunting leads that are investigated by skilled analysts to identify stealthy threats.

All three approaches are a human-powered effort that combines threat intelligence resources with advanced security technology to proactively protect an organization’s systems and information.

Threat Hunting Steps
--------------------
The process of proactive cyber threat hunting typically involves three steps: a trigger, an investigation and a resolution.
### Step 1: The Trigger
**A trigger** points threat hunters to a specific system or area of the network for further investigation when advanced detection tools identify unusual actions that may indicate malicious activity. Often, a hypothesis about a new threat can be the trigger for proactive hunting. For example, a security team may search for advanced threats that use tools like fileless malware to evade existing defenses.
### Step 2: Investigation
During the **investigation phase**, the threat hunter uses technology such as EDR (Endpoint Detection and Response) to take a deep dive into potential malicious compromise of a system. The investigation continues until either the activity is deemed benign or a complete picture of the malicious behavior has been created.
### Step 3: Resolution
**The resolution phase** involves communicating relevant malicious activity intelligence to operations and security teams so they can respond to the incident and mitigate threats. The data gathered about both malicious and benign activity can be fed into automated technology to improve its effectiveness without further human intervention.
Throughout this process, cyber threat hunters gather as much information as possible about an attacker’s actions, methods and goals. They also analyze collected data to determine trends in an organization’s security environment, eliminate current vulnerabilities and make predictions to enhance security in the future.

Resources & Tools
-----------------
- [Threat Hunter Playbook](https://threathunterplaybook.com/intro.html)
- [Roota](https://roota.io/)
- [Uncoder](https://uncoder.io/)
- [Cyber Threat Intelligence (CTI)](https://github.com/MrM8BRH/CRLJ/blob/main/Blue%20Team%20%26%20SOC%20Analyst/Cyber%20Threat%20Intelligence.md)
