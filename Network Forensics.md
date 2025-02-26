# Wireshark
Network analysis tool that captures, analyzes and interpret network traffic.

- Able to extract files from network captures to save and analyze specific object of interest. Useful when extracting files over HTTP, SMD and FTP protocols.

# Zui (Also known as Brim)
GUI Network traffic analysis tool that is able to seamlessly integrate Zeek/Suricata/Wireshark to simplify examining and investigating large network data sets.

1. Examining Suricata alerts through deep packet inspection, traffic analysis and threat detection with Suricata's rule sets to identify suspicious acitivities.
2. Once potential threats are identified, utilize Zeeks log to gain broader overview of network behaviour. Zeek is able to convert raw PCAP files to structured logs.
3. After understanding broader communication behaviours, utilize Wireshark to deep dive into specific packets.


# Extracting IOCs & Objects

## Analyzing HTTP for Reconnaissance and Initial Access Attempts
HTTP transaction logs include data on pages served, data transffered and error logs which have invaluable for tracing attacker activities from reconnaissance to post-compromise actions.

## Analyzing SMB for Lateral Movements Attempts
Able to gain valuable insights into files and other domain-based transaction.  
Possible to determine which files an attacker has viewed, opened, or copied to another location on the network.

## Analyzing DNS for C2 Communications
DNS function as a relay protocol by design which may not prevent a sophisticated DNS tunnel even with strict control over UDP and TCP port 53.
DNS tunneling is also made possible by TXT and NULL records which is ideal for embedding payloads for higher-layer protocols due to the high capacity of arbitrary data storage.

## Analyzing FTP for Data Exfiltration Attempts 
Plaintext protocol commonly used for transferring files, meaning that all data, including username, passwords, and file contents, are transmitted without encryption which makes it easy for attackers to intercept and capture sensitive information. Malicious actors are able to disguise their activities as legitimate file transfers.
