The  report details the analysis of an Ubuntu-based HP EliteBook following a kernel panic, aimed at establishing a SOC development baseline.  
​Integrity: Verified SQLite databases using SHA-256 hashing prior to analysis.  
​Browser Analysis: Investigated places.sqlite and cookies.sqlite from Firefox.  
​SOC Correlation: Frequent visits to localhost/app/wz-home confirmed active Wazuh manager operations, supporting the conclusion that the system is a SOC development environment.  
​Artifact Correlation: Successfully linked recently-used logs with browser history to create a cohesive narrative of system setup and defense monitoring.
