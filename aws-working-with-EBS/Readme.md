# 🚀 AWS EBS Volume Lab Project

## 📌 Project Overview
This project demonstrates how to work with Amazon EBS (Elastic Block Store) by creating, attaching, and managing storage volumes in AWS.

## 🎯 Objectives
- Create an EBS volume
- Attach EBS to EC2 instance
- Mount volume in Linux
- Create snapshot (backup)
- Restore data using snapshot

---

## 🛠️ Services Used
- Amazon EC2
- Amazon EBS
- Amazon S3 (for snapshot storage)

---

## 🧱 Architecture
EC2 Instance → Attached EBS Volume → Snapshot → Restored Volume

---

## ⚙️ Steps Performed

### 1. Created EBS Volume
- Type: gp2
- Size: 1 GiB
- Same Availability Zone as EC2

### 2. Attached Volume to EC2
- Device: /dev/sdb

### 3. Mounted Volume
- File system: ext3
- Mount path: /mnt/data-store

### 4. Created Snapshot
- Backup stored in S3

### 5. Restored Volume
- Created new volume from snapshot
- Attached as /dev/sdc

---

## 💻 Commands Used
See `commands.txt`

---

## 📸 Screenshots
(Add screenshots here)

---

## 📚 Key Learnings
- EBS is block storage for EC2
- Snapshots are incremental backups
- Data persists even after EC2 restart
- Snapshots can restore deleted data

---

## 🚀 Use Case
- Backup and recovery
- Database storage
- Persistent application storage

---

## 🧑‍💻 Author
Your Name