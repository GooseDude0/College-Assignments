IDS and Anomaly Detection

An Intrusion Detection System (IDS) is a tool used to monitor network or system activity for signs of security threats. It helps detect suspicious behavior, such as hacking attempts, malware infections, or unauthorized access. Anomaly detection is a method used by IDS to spot unusual or abnormal activities that stray from normal behavior. This technique is useful for finding new or unknown threats, as it doesn't rely on pre-known attack patterns. IDS can use different methods, including signature-based detection (looking for known attack patterns) and anomaly-based detection (spotting new threats based on unusual behavior). Together, they improve network security by identifying and responding to potential attacks in real time.

How to run Snort for live network monitoring

1. sudo apt install snort
2. You need to choose the network interface (e.g., eth0 or wlan0) for Snort to monitor. You can find the network interface using: ifconfig
3. sudo snort -A console -c /etc/snort/snort.conf -i eth0 (Replace "eth0" with your network interface.)

How to Write and Test Snort Rules

Write a Rule

1. alert icmp any any -> 0.0.0.0 any (msg: "ICMP traffic to 8.8.8.8 detected"; sid:1000001; rev:1;)
Replace the "0.0.0.0" with the destination IP you want.

Save the Rule

1. Save the rule in a file (i.e., /etc/snort/rules/local.rules), and add it to Snort’s configuration file: sudo nano /etc/snort/rules/local.rules
2. To save your changes to the file: CTRL+X , y, ENTER

Test the Rule

1. sudo snort -A console -l /var/log/snort -i enp0s3 -c /etc/snort/snort.conf  -q
2. Hit CTRL + Shift + T on your terminal to open a new terminal.
3. Send a ping to 0.0.0.0 to see if the rule works.

How to Analyze Alert Logs for Threats

1. sudo cat /var/log/snort/alert
2. Look at the alerts to see if the behavior looks suspicious. For example, if you see repeated failed login attempts or strange file requests, these could indicate a security issue.

