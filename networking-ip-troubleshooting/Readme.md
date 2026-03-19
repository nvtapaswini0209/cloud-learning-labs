🌐 AWS Networking Troubleshooting Lab
📌 Overview

This project demonstrates how to troubleshoot network connectivity issues on an Amazon EC2 instance using common Linux networking commands.

It covers multiple layers of the OSI model and simulates real-world cloud support scenarios.

🎯 Objectives

Practice essential network troubleshooting commands

Understand how commands map to OSI layers

Diagnose connectivity, latency, and port issues

Gain hands-on experience with AWS EC2 and Linux

🧰 Tools & Technologies

Amazon EC2 (Amazon Linux)

AWS Management Console

SSH (PuTTY / Terminal)

Linux Networking Commands

🏗️ Architecture

Client (Local Machine)
↓
SSH Connection
↓
Amazon EC2 Instance
↓
Internet (External Servers like 8.8.8.8 / google.com)

🧪 Commands Used
🔹 1. Ping (Layer 3 - Network)

Checks connectivity using ICMP.

ping 8.8.8.8 -c 5
🔹 2. Traceroute (Layer 3 - Network)

Displays path and latency between source and destination.

traceroute 8.8.8.8
🔹 3. Netstat (Layer 4 - Transport)

Shows active connections and listening ports.

netstat -tp
netstat -tlp
🔹 4. Telnet (Layer 4 - Transport)

Tests connectivity to a specific port.

telnet www.google.com 80
🔹 5. Curl (Layer 7 - Application)

Tests HTTP/HTTPS response from a server.

curl -vLo /dev/null https://aws.com
📸 Screenshots

Screenshots are available in the screenshots/ folder:

EC2 Instance Setup

SSH Connection

Ping Output

Traceroute Output

Netstat Output

Telnet Output

Curl Output

🎥 Demo Video

(Add your YouTube video link here)

🧠 Key Learnings

Layer 3 troubleshooting using ping and traceroute

Layer 4 troubleshooting using netstat and telnet

Layer 7 validation using curl

Identifying network issues such as:

Packet loss

Latency

Blocked ports

Connectivity failures

🧩 Real-World Use Cases

Cloud Support Engineer troubleshooting

Diagnosing EC2 connectivity issues

Verifying firewall and security group rules

Debugging web server accessibility

🧪 Sample Test Cases (QA Perspective)
Test Case	Description	Expected Result
Ping Test	Check connectivity to 8.8.8.8	Successful replies
Traceroute	Check network path	Valid hops displayed
Port Test	Check port 80 using telnet	Connection successful
HTTP Test	Verify website response using curl	200 OK response
🚀 Future Improvements

Add automation scripts for testing

Integrate monitoring using CloudWatch

Expand to VPC-based troubleshooting scenarios

📌 Author

Venkata Tapaswini Nallana
Aspiring Cloud + QA Engineer
AWS | Linux | Networking | Testing

⭐ Notes

This project is part of my AWS learning and portfolio development for cloud and QA-related roles.