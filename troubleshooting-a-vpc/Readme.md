# AWS VPC Troubleshooting & Flow Logs Analysis Project

## 📌 Project Overview
This project demonstrates troubleshooting of AWS VPC networking issues and analyzing VPC Flow Logs using AWS CLI.

The lab environment consists of:
- 2 VPCs
- EC2 instances (CLI Host & Web Server)
- Public subnet with misconfigured networking
- VPC Flow Logs stored in S3

---

## 🎯 Objectives
- Create VPC Flow Logs
- Troubleshoot connectivity issues
- Fix Route Table and NACL issues
- Analyze flow logs using CLI tools

---

## 🏗 Architecture
Client → Internet → Internet Gateway → Route Table → Subnet → NACL → EC2 (Web Server)

Flow Logs:
VPC → Flow Logs → S3 → CLI Analysis

---

## 🚨 Issues Identified

### Issue 1: Website not loading
- Cause: Missing route to Internet Gateway in Route Table
- Fix: Added route `0.0.0.0/0 → IGW`

---

### Issue 2: SSH access blocked
- Cause: Network ACL denying port 22
- Fix: Removed DENY rule for port 22

---

## 🛠 Technologies Used
- AWS EC2
- VPC
- Route Tables
- Network ACLs
- Security Groups
- S3
- VPC Flow Logs
- AWS CLI
- Linux (grep, gunzip)

---

## 🔍 Flow Logs Analysis

### Extract logs
```bash
gunzip *.gz
Find rejected traffic
grep -r REJECT .
Find SSH failures
grep -r 22 . | grep REJECT
📊 Key Learnings

Difference between Security Groups and NACLs

Route Table importance for internet access

How to troubleshoot VPC networking issues

Real-time log analysis using CLI

🚀 Outcome

Successfully restored web access

Fixed SSH connectivity

Analyzed rejected traffic using flow logs

💡 Interview Explanation

This project demonstrates hands-on experience in:

AWS networking troubleshooting

Cloud security concepts

Log analysis and debugging

📌 Author

Venkata Tapaswini Nallana