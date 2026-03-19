# AWS Storage Management Project (EBS + S3 + Automation)

## 📌 Project Overview
This project demonstrates how to manage storage in AWS using:
- Amazon EBS Snapshots
- Amazon S3 Sync
- S3 Versioning
- Automation using Cron and Python

---

## 🚀 Architecture
EC2 (Processor)
   ↓
EBS Volume
   ↓
Snapshots (Automated)
   ↓
S3 Bucket (Sync + Versioning)

---

## 🛠️ Services Used
- Amazon EC2
- Amazon EBS
- Amazon S3
- AWS CLI
- IAM Roles
- Cron Jobs
- Python (Boto3)

---

## ⚙️ Features Implemented

### 1. Snapshot Automation
- Created EBS snapshots using AWS CLI
- Automated snapshots every minute using cron
- Retained only last 2 snapshots using Python script

### 2. S3 Sync
- Synced local files to S3 bucket
- Used `--delete` to maintain consistency

### 3. Versioning & Recovery
- Enabled S3 versioning
- Deleted file and recovered previous version

---

## 📂 Commands Used
Refer `commands.txt` for all CLI commands.

---

## 📸 Screenshots
Screenshots available in `/screenshots` folder.

---

## 🎯 Key Learnings
- EBS snapshots are incremental
- S3 versioning helps recover deleted files
- Automation using cron improves reliability
- AWS CLI is powerful for real-world DevOps tasks

---

## 💡 Future Improvements
- Use Lambda instead of cron
- Add CloudWatch monitoring
- Terraform automation

---

## 👩‍💻 Author
Venkata Tapaswini Nallana