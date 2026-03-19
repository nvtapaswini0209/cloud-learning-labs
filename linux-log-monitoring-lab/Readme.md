# AWS Linux Log Monitoring Lab

## Overview
In this lab I connected to an Amazon Linux EC2 instance using SSH and reviewed system authentication logs. This exercise demonstrates how system administrators monitor login attempts and analyze user activity on Linux servers.

## Objectives
- Connect to an EC2 instance using SSH
- Review authentication logs
- Identify login failures
- Check last login activity of users

## Architecture

Local Machine
     │
     │ SSH
     ▼
Amazon EC2 (Amazon Linux)
     │
     ├── Secure Log File
     └── Last Login History

## Lab Steps

1. Start the AWS Lab environment
2. Connect to the EC2 instance using SSH
3. Navigate to the companyA directory
4. Review secure log files
5. Check login history of users

## Commands Used

View current directory
pwd

Navigate to companyA folder

cd companyA

View secure log file

sudo less /tmp/log/secure

Exit log viewer

q

View last login history

sudo lastlog
Key Learnings

Linux servers store authentication activity in secure log files.

The secure log records failed login attempts, source IP addresses, and access ports.

The lastlog command helps administrators audit user login history.

Real World Use Case

System administrators and cloud engineers use secure logs to:

Detect unauthorized login attempts

Investigate security incidents

Monitor user access to servers

Maintain system security compliance

AWS Services Used

Amazon EC2

Amazon Linux

Instance Details

Instance Type: t3.micro
vCPU: 1
Memory: 1 GiB

Demo Video

YouTube Link: (Private Lab Recording)


---

# 📄 commands.txt

Check current directory

pwd

Navigate to companyA directory

cd companyA

View secure authentication logs

sudo less /tmp/log/secure

Exit log viewer

q

View last login activity

sudo lastlog


---

# 📺 YouTube Title

Use something simple and searchable:


AWS EC2 Linux Log Monitoring Lab | Secure Log & Lastlog Command


Alternative:


AWS Linux Security Logs Lab | Monitoring Login Activity on EC2


---

# 📄 YouTube Description


In this AWS lab I connected to an Amazon Linux EC2 instance using SSH and analyzed system authentication logs.

Lab Tasks:
• Connect to EC2 using SSH
• Review secure authentication log file
• Identify failed login attempts
• Check last login history using lastlog command

Commands Used:
pwd
cd companyA
sudo less /tmp/log/secure
sudo lastlog

AWS Services Used:
Amazon EC2
Amazon Linux

Instance Type:
t3.micro

This lab demonstrates how Linux administrators monitor server access and investigate login activity.

#AWS #CloudComputing #Linux #EC2 #AWSLabs


---

# ⭐ Portfolio Tip (Important)

Since you are preparing for **Cloud / DevOps / QA roles**, organize GitHub like this:


cloud-projects
│
├── aws-ec2-web-server-lab
├── aws-ebs-volume-lab
├── aws-linux-log-monitoring-lab
├── aws-vpc-network-lab
└── cloud-resume-challenge


Recruiters **love structured repositories like this**.

---

✅ If you want, I can also give you a **perfect 15-project AWS portfolio structure that impresses recruiters** (most beginners miss this).