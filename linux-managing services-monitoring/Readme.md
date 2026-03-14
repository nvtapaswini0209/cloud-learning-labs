# AWS EC2 Monitoring Lab

## Overview

This lab demonstrates how to monitor an Amazon Linux 2 EC2 instance using both Linux system monitoring tools and AWS CloudWatch.

The goal of this lab is to understand how cloud engineers monitor server performance, verify service status, and observe resource usage during workloads.

---

## Architecture

The architecture includes an Amazon EC2 instance running Apache HTTP Server inside a public subnet. Monitoring is performed using Linux commands and AWS CloudWatch metrics.

User Browser
     |
Internet Gateway
     |
AWS Region
   |
   └── VPC
        |
        └── Public Subnet
              |
              └── EC2 Instance (Amazon Linux 2)
                   Apache httpd Server
                   |
                   |
              Linux Monitoring (top command)
                   |
                   |
              AWS CloudWatch
           CPU / Disk / Network Metrics

Architecture Diagram

![Architecture](architecture/monitoring-architecture.png)

---

## AWS Services Used

- Amazon EC2
- AWS CloudWatch

---

## Instance Details

Instance Type: t3.micro  
Operating System: Amazon Linux 2  
Web Server: Apache HTTP Server (httpd)

---

## Lab Objectives

- Connect to EC2 using SSH
- Check Apache httpd service status
- Start and stop the Apache web server
- Verify the web server through a browser
- Monitor running processes using Linux top command
- Simulate CPU load using a stress script
- Analyze EC2 performance metrics using AWS CloudWatch

---

## Key Linux Commands Used

Check Apache service status

sudo systemctl status httpd.service

Start Apache service

sudo systemctl start httpd.service

Stop Apache service

sudo systemctl stop httpd.service

Display running processes and system usage

top

Run CPU stress test

./stress.sh & top

---

## Monitoring with CloudWatch

AWS CloudWatch automatically collects metrics from EC2 instances such as:

- CPU Utilization
- Disk Read Operations
- Disk Write Operations
- Network Traffic

During the lab, a CPU workload was generated using a stress script to observe how CloudWatch captures the increase in CPU utilization.

---

## Screenshots

| Step | Description |
|-----|-------------|
| EC2 Instance Running | EC2 instance launched |
| SSH Connection | Connected to EC2 via SSH |
| httpd Inactive | Apache service status inactive |
| httpd Active | Apache service started |
| Apache Test Page | Web server verified via public IP |
| Linux top Command | Viewing system processes |
| CPU Stress Test | Simulated workload |
| CloudWatch Dashboard | Monitoring metrics |
| CPU Utilization Spike | CPU usage increase observed |

Screenshots are available in the **screenshots** folder.

---

## Demo Video

Full lab demonstration:

YouTube Link: (Add your video link here)

---

## Key Learning Outcomes

- Managing Linux services on EC2
- Monitoring system processes
- Understanding CPU utilization during workloads
- Using AWS CloudWatch for cloud monitoring
- Observing system metrics in real-time

---

## Repository Structure

aws-hands-on-labs  
│  
├── ec2-monitoring-lab  
│   ├── README.md  
│   ├── architecture  
│   │   └── monitoring-architecture.png  
│   ├── screenshots  
│   ├── commands  
│   │   └── monitoring-commands.md  
│   └── videos  

---

## Author

Venkata Tapaswini Nallana  
Cloud / QA / DevOps Enthusiast