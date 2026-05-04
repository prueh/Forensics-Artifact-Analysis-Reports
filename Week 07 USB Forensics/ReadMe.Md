The first phase involved the forensic examination of a 16GB physical USB drive to identify potential threats and verify its contents.  
​Acquisition: Used AccessData FTK Imager to capture a bit-stream image in .E01 format, ensuring data integrity with MD5/SHA1 hashing.  
​Methodology: Analysis was performed in a virtualized Windows 10 environment using Autopsy 4.23.0. Modules included Solr indexing for keyword searches and PhotoRec for data carving.  
​Key Findings:
​The media was identified as a non-malicious Ubuntu Installation ISO.  
​Targeted searches for malware (njRAT, Wannacry) returned zero matches.  
​Suspicious modules flagged by the tool were validated as legitimate GRUB components for encrypted partitions.  
