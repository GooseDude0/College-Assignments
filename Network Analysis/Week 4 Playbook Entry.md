The 4 layers of the TCP/IP Model
  1. Application Layer
        Provides various network services to applications (HTTP, FTP, DNS, etc.)
        Used when applications need network communication (web browsing, email, file transfer, etc.)
  2. Transport Layer
        Manages end-to-end communication between devices.
        Uses TCP or UDP.
        Ensures data integrity, flow control, and retransmission if necessary.
  3. Internet Layer
        Handles logical addressing and routing of packets.
        Uses IPv4 & IPv6 for addressing and routing and ICMP for diagnostics.
        Ensures that packets reach the correct destinations.
  4. Network Access Layer
        Manages physical transmission and MAC addressing.
        Uses Ethernet, Wi-Fi, ARP, and PPP to send data over physical media.
        Ensures device-to-device communication within a local network.

Options for following streams in Wireshark
  1. Follow TCP Stream
        Reconstructs TCP-based communication (HTTP, FTP, SSH).
        Useful for analysing entire coversations between a client and server.
  3. Follow HTTP Stream
        Extracts and displays HTTP traffic between client and server.
        Useful for troubleshooting web requests and inspecting responses.

Checklist for anomaly detection
  1. Unusual Traffic Patterns?
        Sudden spikes in network traffic?
        High amount of outbound connections?
  2. Unrecognized IP Addresses?
        Connections to malicious or unknown IPs?
        Unexpected external communications?
  3. Unusaul Port Activity?
        Traffic on non-standard ports (SSH on 8080)?
        Unexpected open or closed ports?
  4. Packet Anomalies?
        Malformed packets or unusual flag combinations?
        Large payloads or unexpected retransmissions?
  5. Unauthorized Access Attemps?
        Repeated failed logins (brute force attacks)?
        Sudden privilege escalations?
  6. Unusual Protocol Usage?
        HTTP traffic in a normally encrypted session?
        Unexpected FTP transfers?
  7. Strange Behavior in Logs?
        Unexpected commands executed?
        Log files being deleted or modified?

