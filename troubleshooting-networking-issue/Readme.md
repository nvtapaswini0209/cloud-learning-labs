# AWS VPC Troubleshooting Lab – Apache Server Not Accessible

## 📌 Project Overview
This lab demonstrates how to troubleshoot a networking issue in AWS where an Apache web server is running but not accessible via browser.

## 🧠 Problem
- Apache server is active
- Instance has public IP
- Cannot access via browser

## 🔍 Root Cause
Security Group did not allow HTTP (port 80), blocking incoming traffic.

## 🏗️ Architecture
VPC → Public Subnet → Internet Gateway → EC2 Instance (Apache)

## 🛠️ Steps Performed

### 1. Connect to EC2
- Used SSH to access instance

### 2. Install Apache
- Started httpd service

### 3. Tested Connectivity
- Ping to internet successful
- Browser access failed

### 4. Troubleshooting
- Verified Internet Gateway
- Checked Route Table
- Confirmed subnet association
- Fixed Security Group

### 5. Fix Applied
Added inbound rule:
- HTTP (port 80) → 0.0.0.0/0

## ✅ Result
Apache test page successfully loaded in browser.

## 📚 Key Learnings
- Security Groups control inbound traffic
- Route Tables manage routing
- Internet Gateway enables internet access
- Troubleshooting requires step-by-step validation

## 🎯 Real-World Use Case
Cloud engineers frequently debug similar issues when applications are unreachable.

## 📹 Demo Video
(Add your YouTube link here)
