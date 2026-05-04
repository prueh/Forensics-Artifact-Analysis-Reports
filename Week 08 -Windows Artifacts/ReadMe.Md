This investigation focused on establishing a verifiable timeline of activity on a Windows 10 workstation.  
​Tooling: Utilized Eric Zimmerman’s EvtxECmd to parse Windows Security Event Logs into structured CSV data.  
​Living off the Land: In the absence of standard GUI tools, PowerShell (Import-Csv and Out-GridView) was used to filter thousands of records.  
​The "Smoking Gun": Identified Event ID 4624 (Logon Type 2) at Record ID 50, confirming the exact moment of authorized interactive access by a human user.  
​Technical Audit: Investigated a lack of Prefetch artifacts and discovered the SysMain service had been disabled to conserve VM resources, explaining the discrepancy. 
