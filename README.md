# Forensics-Artifact-Analysis-Reports
Digital Forensics, Incident Response (DFIR), and System Baselining.
Project Overview: Forensic Artifact Analysis
​Analyst: Prudence Nthenya
Timeline: April - May 2026
Focus: Digital Forensics, Incident Response (DFIR), and System Baselining.
​Phase 1: Digital Media & Malware Triage (Week 7)
​The first phase involved the forensic examination of a 16GB physical USB drive to identify potential threats and verify its contents.  
​Acquisition: Used AccessData FTK Imager to capture a bit-stream image in .E01 format, ensuring data integrity with MD5/SHA1 hashing.  
​Methodology: Analysis was performed in a virtualized Windows 10 environment using Autopsy 4.23.0. Modules included Solr indexing for keyword searches and PhotoRec for data carving.  
​Key Findings:
​The media was identified as a non-malicious Ubuntu Installation ISO.  
​Targeted searches for malware (njRAT, Wannacry) returned zero matches.  
​Suspicious modules flagged by the tool were validated as legitimate GRUB components for encrypted partitions.  
​Phase 2: Windows Host Forensics & Human Baselining (Week 8)
​This investigation focused on establishing a verifiable timeline of activity on a Windows 10 workstation.  
​Tooling: Utilized Eric Zimmerman’s EvtxECmd to parse Windows Security Event Logs into structured CSV data.  
​Living off the Land: In the absence of standard GUI tools, PowerShell (Import-Csv and Out-GridView) was used to filter thousands of records.  
​The "Smoking Gun": Identified Event ID 4624 (Logon Type 2) at Record ID 50, confirming the exact moment of authorized interactive access by a human user.  
​Technical Audit: Investigated a lack of Prefetch artifacts and discovered the SysMain service had been disabled to conserve VM resources, explaining the discrepancy.  
​Phase 3: Linux Browser Forensics & SOC Baselining (Week 9)
​The final report details the analysis of an Ubuntu-based HP EliteBook following a kernel panic, aimed at establishing a SOC development baseline.  
​Integrity: Verified SQLite databases using SHA-256 hashing prior to analysis.  
​Browser Analysis: Investigated places.sqlite and cookies.sqlite from Firefox.  
​SOC Correlation: Frequent visits to localhost/app/wz-home confirmed active Wazuh manager operations, supporting the conclusion that the system is a SOC development environment.  
​Artifact Correlation: Successfully linked recently-used logs with browser history to create a cohesive narrative of system setup and defense monitoring.  
