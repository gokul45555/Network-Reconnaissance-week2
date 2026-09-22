Week 2 – Penetration Testing Lab
Author: Gokul R
Course: B.Sc. Computer Science with Cyber Security
Platform: Kali Linux
Tools: theHarvester, Nmap, Zenmap
Date: 22 September 2026
📌 Overview
This project documents Week 2 of my penetration testing lab.
The objective was to perform:
Passive reconnaissance using theHarvester
Active host discovery using Nmap/Zenmap
All testing was performed in an isolated lab environment for academic purposes.
Sensitive target-domain and internal IP information has been redacted.
🎯 Objectives
Understand passive reconnaissance.
Gather publicly available information using theHarvester.
Identify subdomains and hosts from OSINT sources.
Perform active host discovery using Nmap/Zenmap.
Understand basic network reconnaissance techniques.
Document penetration testing results.
🛠️ Tools Used
Tool
Purpose
theHarvester v4.10.1
OSINT gathering and subdomain enumeration
Nmap 7.991
Network scanning and host discovery
Zenmap
Graphical interface for Nmap
Kali Linux
Penetration testing environment
🔎 Part A – Passive Reconnaissance
theHarvester
theHarvester was used to passively gather information about the target domain from open-source intelligence sources.
The target domain has been redacted as:
<target-domain>
Command Used
theHarvester -d <target-domain> -l 50 -b all
Results
The scan discovered multiple subdomains and hosts through available OSINT sources.
Some sources returned "Missing API key" errors because API keys were not configured.
Affected sources included:
bevigil
Bitbucket
bufferoverun
BuiltWith
SecurityScorecard
🔍 Baidu Source Scan
A source-specific scan was also performed:
theHarvester -d <target-domain> -l 1000 -b baidu
Result
No IP addresses, emails, people, or hosts were returned.
This showed that different OSINT sources can provide different levels of information.
🌐 Part B – Active Host Discovery
Nmap / Zenmap
Zenmap was used to perform a ping sweep across the lab subnet.
Scan Profile
Ping scan
Nmap Command
nmap -sn <subnet>/24
The -sn option performs host discovery without scanning ports.
Results
Network range: /24
Possible addresses: 256
Scan time: 8.12 seconds
Live hosts discovered: 2
One host returned a resolvable MAC address.
🗺️ Network Topology
Zenmap's Topology tab was used to visualize the discovered hosts.
The discovered hosts appeared as directly connected nodes on the same local network as the scanning machine.
Sensitive IP addresses have been redacted.
📊 Findings
Multiple subdomains were discovered through OSINT sources.
Several theHarvester sources required API keys.
The Baidu source returned no useful results.
The Nmap/Zenmap ping sweep identified 2 live hosts on the lab subnet.
💡 Recommendations
Configure API keys for additional OSINT sources.
Cross-check information using multiple reconnaissance sources.
Perform authorized port and service enumeration on discovered lab hosts.
Regularly review publicly discoverable subdomains.
Protect sensitive network and infrastructure information.
📚 Learning Outcomes
Through this project, I learned:
Basics of passive reconnaissance.
How OSINT can reveal publicly available information.
How to use theHarvester.
How to perform host discovery using Nmap.
How to use Zenmap for network discovery.
How to analyze basic reconnaissance results.
The importance of responsible and authorized security testing.
⚠️ Ethical & Legal Notice
This project was performed only in an isolated lab environment for educational purposes.
The techniques demonstrated should only be used on systems and networks where proper authorization has been obtained.
Sensitive target information has been redacted.
👨‍💻 Author
Gokul R
B.Sc. Computer Science with Cyber Security
