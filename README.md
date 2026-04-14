# SOC Investigation: HTTP Beaconing & Reverse Shell Activity Analysis (PCAP)

* **Scenario:** Analyzed a PCAP of an internal host communicating with a malicious C2 server.
* **Findings:** Identified a reverse shell and persistence via crontab.
* **Tools:** Wireshark, Base64 Decoding, Linux Shell Analysis.

## Detection & Mitigation
* **Network Detection:** Alert on excessive HTTP GET requests to external IPs and outbound traffic on non-standard ports (e.g., TCP 1337).
* **Endpoint Detection:** Monitor for unauthorized `socat` execution and modifications to `.bashrc` or `.profile`.
* **Remediation:** Enforce **Principle of Least Privilege (PoLP)** and implement egress filtering to block unauthorized outbound traffic.

## Technical Report
[View the Full Technical Analysis Report Here](./SOC%20Investigation%20PCAP.md)
