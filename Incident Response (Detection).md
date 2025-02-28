# Suricata

Network Security Monitoring (NSM) tool that acts as both Intrusion Detection System (IDS) and Intrusion Prevention System (IPS).  

- Deployable on machines or gateways to perform live inspection of network traffic, or offline packet capture (PCAPS) for malicious activity.  
- Able to analyse inbound/outbound traffic, alerts on threats and actively block attacks when configured as Intrusion Prvention System (IPS).

# RITA (Real Intelligence Threat Analytics)

Designed to identify Command-and-Control (C2) communications by analysing network traffic patterns based on behavioral anomalies (such as long-lived connections, beaconing intervals, DNS tunneling, traffic to known malicious IPs) instead of signature-based tools.

1. Create new Folder ($mkdir "foldername")
2. Convert PCAP files into Zeek logs. ($zeek -r "filename.pcap" local)  -- This will create 13 Zeek logs files into the new folder created previously.
3. Import Zeek logs into RITA ($sudo rita import "foldername" "datasetname")  -- This will create a dataset named "datasetname" in MongoDB for RITA to process and analyse.

To generate a report to .html file for visuals  
($rita html-report "datasetname")

# Sysmon (System Monitor)
Lightweight monitoring tool to enhance visibility and detection capabilities.  

- Able to detect attacker actions such as malicious process execution and persistence mechanisms and more.

# Velociraptor
Digital Forensics and Incident Response (DFIR) platform designed to collect data, monitor activity, and hunt threats across endpoints or entire networks.

- Able to collect artifact such as identifying evidence of file downloads which provides Downloaded filenames and path, Source URLS, Timestamps of download activity.  
- Able to capture memory dump for an infected process to provide malware runtime behaviour (Injected code, Encryption keys) which are often missed by disk forensics. Dumps can then be analysed with tools such as Volatility or Rekall.
