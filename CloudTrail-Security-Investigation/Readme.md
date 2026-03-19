# AWS CloudTrail Security Investigation Lab

## Project Overview

This project demonstrates how to investigate a security incident in AWS using CloudTrail logs, AWS CLI, Linux commands, and Amazon Athena.

A simulated hacking scenario was performed on a Café website hosted on an Amazon EC2 instance. The goal of the investigation was to identify the attacker, analyze how the breach occurred, and secure the environment.

---

## Architecture

EC2 Web Server
      │
Security Group Modified
      │
CloudTrail Logs Generated
      │
Logs Stored in S3
      │
Analyzed using:
• Linux grep
• AWS CLI
• Amazon Athena

---

## AWS Services Used

- Amazon EC2
- AWS CloudTrail
- Amazon S3
- Amazon Athena
- AWS CLI
- IAM

---

## Investigation Steps

1. Launch EC2 web server
2. Configure security group
3. Enable CloudTrail logging
4. Detect unauthorized modification
5. Download logs from S3
6. Analyze logs using grep
7. Investigate with AWS CLI
8. Query logs using Athena
9. Identify hacker
10. Remove malicious user
11. Secure SSH configuration
12. Restore website

---

## Key Skills Demonstrated

Cloud security investigation  
Log analysis  
AWS monitoring  
Incident response  
Security best practices

---

## Outcome

The hacker was identified through CloudTrail logs and Athena queries. Unauthorized access was removed and the EC2 instance was secured.

---

## Video Walkthrough

YouTube: (Add your video link here)