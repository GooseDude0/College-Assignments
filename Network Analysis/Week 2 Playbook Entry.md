Deep Packet Inspection (DPI) is a way to look at network traffic in detail. It helps find security threats, data leaks, and other issues. Unlike basic filtering, DPI checks the actual content of data packets. This makes it useful for spotting harmful activity, enforcing rules, and fixing network problems. Tools like Wireshark help analyze these packets and understand network behavior.

How to Filter DNS Traffic in Wireshark

Open Wireshark and load a packet capture file. In the Filter bar, type dns and press Enter. This should show only DNS request and response packets. Click on a DNS packet to see details like requested domain names and response IPs.

How to Filter FTP Traffic & Check User Logins

In Wireshark, type ftp in the Filter bar and press Enter. Look for packets with USER and PASS commands, which show login attempts. Click on a packet to check details like usernames and login results. Look at server responses to see if logins failed or files were transferred.

How to Inspect ICMP Messages

In the Filter bar, type icmp and press Enter. Should will now show only ICMP packets, such as ping requests and replies. Click on a packet to see details like source and destination IPs, size, and response time.
