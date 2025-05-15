# SOC Tools and Their Features

A Security Operations Center (SOC) relies on a supporting infrastructure of tools and systems that provide the following services:

- **Network mapping**
- **Network monitoring**
- **Vulnerability detection**
- **Penetration testing**
- **Data collection**
- **Threat and anomaly detection**
- **Data aggregation and correlation**

---

## Security Onion

One tool that is used by analysts in a SOC is **Security Onion**.

Security Onion is designed to support SOC analysts with a suite of tools for:

- Intrusion Detection
- Network Security Monitoring (NSM)
- Log Management

It is based on **Ubuntu Linux** and includes security tools delivering four core NSM functions:

- **Full packet capture**
- **Network- and host-based intrusion detection sensors**
- **Security analysis tools**
- **Log management**

---

### ELSA Stack Components (Legacy Version)

The **Enterprise Log Search and Archive (ELSA)** version includes:

#### 🔹 ELSA  
- Centralized syslog framework built on Syslog-NG, MySQL, and Sphinx  
- Fully asynchronous web-based query interface  
- Supports: normalized logs, billions of record searches, permissions, alerts, scheduled queries, graphing  

#### 🔹 Snort  
- Open source, rule-driven NIDS/NIPS by Cisco (Sourcefire)  
- Real-time threat detection and alerting  
- NIPS inline mode **not supported** in Security Onion  

#### 🔹 Suricata  
- Script-driven NIDS/NIPS engine  
- Supports threat detection and alert generation  
- NIPS inline mode **not supported** in Security Onion  

#### 🔹 Zeek (formerly Bro)  
- Packet recorder and protocol parsing engine  
- Detects behavioral anomalies  

#### 🔹 Traffic Logging  
- Uses SPAN, TAP port, or packet broker  
- Logs over 35 protocols including HTTP, DNS, FTP, SMTP  

#### 🔹 Automated Analysis  
- Performs traffic analysis using Bro (Zeek) scripts  

#### 🔹 File Extraction  
- Extracts and reassembles file types directly from network traffic  

#### 🔹 Wazuh (OSSEC Replacement)  
- Host-based intrusion detection system (HIDS)  
- Lightweight agent for Windows, Linux, Mac OS X, HP-UX, AIX, Solaris  

#### 🔹 Netsniff-ng  
- Captures traffic (SPAN, TAP, packet broker) as PCAP files  

#### 🔹 Sysmon  
- Monitors Windows system activity and event logs  

#### 🔹 Syslog-ng  
- Enhanced BSD log daemon for collecting logs from diverse sources  

---

### Network Analyst Tools

Included in Security Onion to support SOC functions:

#### 🔹 Wireshark  
- Widely-used network protocol analyzer  

#### 🔹 Sguil  
- Real-time network security monitoring GUI  
- Displays alerts, session data, and packet captures  

#### 🔹 Squert  
- Web application that queries and visualizes Sguil alert data  
- Offers metadata views, time series, and logical groupings  

#### 🔹 NetworkMiner  
- Parses PCAP files and extracts artifacts  

#### 🔹 CyberChef  
- Web-based platform for data manipulation and transformation  

#### 🔹 CapME  
- PCAP transcript analysis and capture file download  

---

### Example Workflow

Tools work in tandem to provide layered visibility:

- **IDS alerts** from Snort or Suricata  
- Analysts query logs via **ELSA** to validate IDS messages  
- **Sguil** provides real-time visualization of session and alert data  

These tools collectively empower security analysts to investigate and respond to threats effectively.

---

## Security Onion 2 (Elastic Stack Version)

The newer version of Security Onion is built on the **Elastic Stack (ELK)** and includes the following tools:

#### 🔹 Elasticsearch  
- Scalable log indexing and search engine based on Apache Lucene  

#### 🔹 Logstash  
- Data ingestion and parsing pipeline  

#### 🔹 Kibana  
- Web-based dashboard and visualization for Elasticsearch data  
- Can pivot to CapME for full packet capture access  

#### 🔹 TheHIVE  
- Security incident response and case management  
- Integrated with **MISP** (Malware Information Sharing Platform)  

#### 🔹 Elastic Beats  
- Lightweight shippers for system and application telemetry  

#### 🔹 Curator  
- Elasticsearch index lifecycle and maintenance management  

#### 🔹 ElastAlert  
- Rule-based alerting from Elasticsearch data  

#### 🔹 FreqServer  
- Detects domain generation algorithms (DGAs) and unusual naming patterns  

#### 🔹 DomainStats  
- WHOIS lookups with contextual data such as age, reputation, creation date  

---



##  Summary

Security Onion provides a robust platform for SOC operations. Whether using the legacy ELSA stack or the modern ELK-based system, analysts are equipped with tools to:

- Detect
- Investigate
- Correlate
- Respond to network intrusions in real time

By leveraging these integrated tools, a SOC can achieve continuous visibility, proactive threat hunting, and incident response at scale.





