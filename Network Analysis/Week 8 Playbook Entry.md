This investigation focused on finding the source of a cyber attack using packet capture (PCAP) files. The attack came through an anonymous email service. We used tools like Wireshark to track the sender’s IP and MAC addresses, leading to the attacker’s identification. This tool helped us analyze email details and web traffic.

Common Attack Methods & Their Signs

Phishing Emails

Signs:
Emails from anonymous services (sendanonymousemail.net, willselfdestruct.com)
Suspicious HTTP requests in network traffic
Unusual email traffic

Tracking IP & MAC Addresses

Signs:
Tracing communication between attacker and network
Identifying hardware through MAC addresses

Checking Web Traffic

Signs:
HTTP requests showing visits to suspicious sites
Email addresses in packet details
Filtering packets to find attack patterns ("frame contains '@gmail.com'")

Network Bridges & Dorm Networks

Signs:
Private IPs acting as middle points
Network bridges linking attacker’s device to external networks

Step-by-Step Response Plan

Collect Initial Data: 
Get PCAP files and verify their authenticity.
Count the total packets and the capture duration.

Find Suspicious IPs & MAC Addresses: 
Look for external IPs communicating with internal devices.
Match MAC addresses to their manufacturers.

Analyze Emails & Web Traffic: 

Use Wireshark filters: 
frame contains "@gmail.com" && eth.addr == [Attacker MAC] && http
frame matches "[Victim Email]"

Look for emails sent through anonymous services.

Confirm the Attacker’s Identity: 
Compare IPs, MAC addresses, and email details.
Check login timestamps and source addresses.

Prevent Future Attacks:
Block anonymous mailing services.
Monitor networks for strange email and web activity.
Separate networks to prevent easy access.
Require multi-factor authentication for security.
