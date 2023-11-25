Network Detection and Response (NDR)
------------------------------------
formerly Network Security Monitoring (NSM)

Network detection and response (NDR) is a category of cybersecurity technologies that use non-signature-based methods—such as artificial intelligence, machine learning and behavioral analytics—to detect suspicious or malicious activity on the network and respond to cyber threats. 

NDR evolved from network traffic analysis (NTA), a technology originally developed to extract network traffic models from raw network traffic data. As NTA solutions added behavioral analysis and threat response capabilities, industry analyst Gartner renamed the category NDR in 2020.


Endpoint Detection and Response (EDR)
-------------------------------------
formerly Continuous Security Monitoring (CSM)

Endpoint detection and response, or EDR, is software designed to automatically protect an organization's end users, endpoint devices and IT assets against cyberthreats that get past antivirus software and other traditional endpoint security tools. 

EDR collects data continuously from all endpoints on the network - desktop and laptop computers, servers, mobile devices, IoT (Internet of Things) devices and more. It analyzes this data in real time for evidence of known or suspected cyberthreats, and can respond automatically to prevent or minimize damage from threats it identifies.

![EDR-NDR](https://github.com/MrM8BRH/MrM8BRH/assets/34133187/ba069723-2b87-4e79-ba0d-2a9efc4c624b)

Clarification on Anomaly Detection
------------------------------------
In the realm of cybersecurity, it's essential to recognize that every malicious activity is inherently an anomaly. However, anomalies themselves can take various forms, extending beyond just malicious behavior. Here's a breakdown:

- **Each Malicious Activity is an Anomaly:**
  - Malicious actions, by their nature, deviate from normal patterns and are thus categorized as anomalies.

- **Types of Anomalies:**
  - Anomalies can manifest as:
    - **Malicious Behavior:** Actions indicating a security threat.
    - **Policy Violations:** Instances where actions breach established security policies.
    - **Service or Server Disruptions:** Anomalies related to service downtime or server disruptions.
    - **Other Deviations:** Any behavior outside the established norm.

Analysis Techniques
-------------------
- Stack Analysis
- Frequency Analysis
- Long Tail Analysis

Data Sources
------------
#### 1. NetFlow / Statistical Data
- **Data Elements:**
  - Src IP, Dst IP, Src Port, Dst Port, Protocol, Bytes
- **Analysis Techniques:**
  - Baseline Detection
  - Profiling
  - Spike Analysis
- **Purpose:**
  - Providing insights into network traffic patterns and identifying deviations from the norm.

<div align="center">
  
  ![netflow](https://github.com/MrM8BRH/MrM8BRH/assets/34133187/a11ca926-60fc-4fcd-b986-030c17f7b2a9)
  
</div>

#### 2. Metadata / Packet String (PSTR)
- **Data Content:**
  - Information extracted from packet headers, often in a human-readable format.
- **Analysis Focus:**
  - Examining packet-level details to understand communication patterns and potential anomalies.
- **Use Case:**
  - Enhancing visibility into network activities beyond statistical data.

<div align="center">
  
  ![metadata](https://github.com/MrM8BRH/MrM8BRH/assets/34133187/6a246a8e-84a1-41ae-8890-78946c732654)
  
</div>

#### 3. Full Packet Capture
- **Data Captured:**
  - Complete packet content, including payload data.
- **Analysis Depth:**
  - In-depth analysis of packet contents for comprehensive understanding.
- **Significance:**
  - Providing detailed information for forensic analysis and investigation.

Span Port / Network Tap

<div align="center">
  
  ![nettap](https://github.com/MrM8BRH/MrM8BRH/assets/34133187/b8af889f-66e7-40c0-9a6a-f8f9bac726ed)
  
</div>

**Proper tool placement and comprehensive visibility are critical aspects of a cybersecurity infrastructure. The strategic deployment of monitoring tools ensures maximum coverage and detection capabilities.**
