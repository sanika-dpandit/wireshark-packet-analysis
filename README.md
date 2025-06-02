# wireshark-packet-analysis
# Task 5: Capture and Analyze Network Traffic Using Wireshark

Objective
The goal of this task was to perform a live packet capture using Wireshark, identify different network protocols, and develop hands-on skills in protocol analysis and network troubleshooting.

Tools Used
Wireshark
Operating System
Browser/Command Line: Used to generate HTTP, DNS, and TCP traffic

Steps Followed

1. Installed and opened Wireshark.
2. Started capturing packets on the active network interface.
3. Generated traffic by:
   - Visiting websites using a web browser (to capture HTTP traffic).
   - Running `ping google.com` (to capture ICMP and DNS traffic).
4. Stopped the capture after approximately one minute.
5. Used protocol filters (`http`, `dns`, `tcp`) to isolate specific traffic.
6. Saved the capture file as `network_capture.pcapng`.
7. Analyzed packets to identify and summarize at least three protocols.

Protocols Identified
HTTP (HyperText Transfer Protocol)
-Port: 80 (TCP)
- Description: Used for loading web pages from servers to browsers. The HTTP GET and response packets were visible, showing unencrypted content including URLs and headers.

DNS (Domain Name System)
-Port: 53 (UDP)
-Description: DNS queries were sent to resolve domain names (e.g., `google.com`) into IP addresses. Responses returned the mapped IPs.

TCP (Transmission Control Protocol)
- Ports: Varying (common: 80, 443)
- Description: TCP is a reliable, connection-oriented protocol. The 3-way handshake (SYN, SYN-ACK, ACK) was visible, establishing connections for both HTTP and DNS traffic.

Summary

This task helped build foundational skills in using Wireshark for real-time packet analysis. By analyzing captured traffic, I learned to recognize different protocols, interpret network behavior, and understand the structure of DNS, HTTP, and TCP packets. These skills are essential for troubleshooting network issues and conducting cybersecurity investigations.

Useful Filters Used
http
dns
tcp
tcp.port == 80
udp.port == 53
