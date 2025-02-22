Zeek (formerly known as Bro) is a powerful open-source network security monitoring tool that captures and analyzes network traffic in real time. It generates detailed logs of network activity, enabling security analysts to detect anomalies, investigate threats, and improve incident response. Zeek logs, such as conn.log, dns.log, http.log, ssl.log, and weird.log, provide structured insights into network behavior, allowing for in-depth forensic analysis and threat detection.

Analyzing conn.log for Active Connections

Navigate to the Zeek log directory:
cd /var/log/zeek/

Use cat or less to view the log:
cat conn.log | less

Filter connections using grep:
grep 'ESTABLISHED' conn.log

Extract specific fields with zeek-cut:
cat conn.log | zeek-cut id.orig_h id.resp_h proto service duration state

Find long-duration connections:
awk '$9 > 60' conn.log

Checking dns.log for Malicious Queries

Navigate to the log directory:
cd /var/log/zeek/

View the log with less:
cat dns.log | less

Search for a specific domain:
grep 'malicious-domain.com' dns.log

Identify high query volumes:
awk '{print $3}' dns.log | sort | uniq -c | sort -nr | head

Detect DNS tunneling by filtering for excessive TXT queries:
grep 'TXT' dns.log | wc -l

Identifying Anomalies in http.log, ssl.log, weird.log

http.log:

Look for unusual status codes:
grep -E ' 500 | 404 ' http.log

Identify uncommon user-agents:
cat http.log | awk '{print $9}' | sort | uniq -c | sort -nr | head

ssl.log:

Find expired or self-signed certificates:
grep 'self-signed' ssl.log

Identify weak ciphers:
grep -E 'TLS_RSA|TLS_ECDH' ssl.log

weird.log:

Investigate protocol anomalies:
cat weird.log | grep -i 'malformed'

Detect incomplete handshakes:
grep 'handshake' weird.log
