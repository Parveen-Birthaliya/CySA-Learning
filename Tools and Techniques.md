## Tools and Techniques
#### Wireshark
- Open Source grphical utility
- network traffic analysis

#### tcpdump
- command line utility
- tcpdump -i eth

#### Endpoint Detection and Response
- Malware detection
- URL Filtering
- Honeypots
- Monitoring
- Orchestration
- Alligned with NIST
- AI & ML , Cloud

### DNS and IP reputation
**Whois**
- Domain and IP lookup
- identify malcicious domains

**AbuseIPDB**
- Database of suspicious IP addresses
- Feature: API,SOAR integration
  
### File Analysis
**String**
Extracts viewable character from binaries

**VirusTotal**
- Multi-engine file & URL scanning
- Provides : Malware types,vendor names, indicators,hashes

### Sandboxing
- Isolates untrusted data in a closed environment
- Monitor system changes
- executes known malware files
- Take snapshots
- Monitor network sockets
- Record file creation & deletion
- Dump VM memory
- Monitor system & API calls

**Solutions**
- Joe Sandbox
- Crowdstrike
- Cuckoo Sandbox


### SIEM
- Near real time analysis of security alerts
- aggregation: Unfied data view
- Correlation : Links enterprise -wide events
- Alerting: Automated events analysis
- Visibility : Dashboard view
- Compliance : Goverment & auditing
- Data Retention: Historical data storage



### SOAR
- Automate routine security tasks
- Cloud and SDN/SDV APIs
- Automated Malware Signature creation
- Cyber threat Intelligence Feeds
- AbuseIPDB API


## Common Techniques for Detection
### Understanding Email Message Internet Header Analysis
**Email Routing**
- SMTP protocol
- MDA adds/ammends header
- DNS used for routing MTA

**Header Exploitation
- Spoofed "Display From" to deceive user
- "Received from/by" reveals the true origin

**User interaction**
- View through properties/options/sources

**Header Parsing tools**
- Message Analyzer Tool
- Alert machanism for malicious header

**Custom Headers**
- X-headers
- Used for message authentication and spam analysis

**Types of Malicious Payloads
- Exploits:Targets vulnerabilities in email client
- Attachment:File designed to trick te user into opening

**Email Signature Block**
- Role in phishing and spear phishing
- Can be used to embed malicious link

**Malicious Attachment**
- Antimalware measures
- Limitations and bypasses

**Hash Analysis
- Unique file identtification
- Custom detection rules

**Domain-based Message Authentication,Reporting, and Confermance(DMARC)**
- SPF & DKIM Efficacy
- DMARC Policy
- Reporting Mechansims
- Six stteps to analyze email monitoring output


**Important Powershell Commands**
- Invoke-Request, Invoke-WebRequest
- DownloadString, Start-Process
- Get-WMIObject, Get-Process

**Improtant Linux Commands**
- ssh, wget, curl
- telnet,ftp
- arp, ss, ip, ifconfig
- whoami, netstat

**Imprtant Windows Commands**
- netstat, ping, ipconfig
- nslookup, tasklist
- net, netsh, wmic

  
