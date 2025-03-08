Threat hunting means actively looking for cyber threats before they cause any damage. Instead of waiting for security alerts, people check network traffic for unusual activity that may indicate an attack. Tools like Wireshark help them find hidden threats, track malware communication, and stop data breaches early.

How to Filter DNS Traffic to Find Malicious Queries

Open Wireshark and load the packet capture file. In the Filter bar, type dns and press Enter. Look for suspicious domain requests, such as: Random, strange domain names (e.g., abc123xyz.com), repeated requests to unknown domains, and queries to known malicious websites (check threat lists). Right-click on a suspicious DNS request and follow the TCP stream for more details.

How to Detect Data Theft (Exfiltration)

In Wireshark, type tcp and frame.len > 1000 in the Filter bar and press Enter. This should show large data transfers, which may indicate stolen data being sent out. Look for repeated large packets sent to outside IP addresses. Check for encrypted traffic going to unknown locations, as this could mean stolen data is being sent secretly.

How to Identify C2 (Command & Control) Communication

Find a suspicious external IP address from your analysis or threat reports. Use the filter ip.dst == x.x.x.x, replacing x.x.x.x with the suspect C2 server’s IP. Look for patterns such as:

Repeated connections at fixed time intervals (i.e. every 10 minutes).

Small, frequent packets used to stay hidden.

Encrypted or unknown protocol traffic.
