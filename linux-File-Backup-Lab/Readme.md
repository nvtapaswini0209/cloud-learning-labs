# AWS Linux Lab – Working with Files (Backup Using tar)

## Overview

This lab demonstrates how to create and manage backups of a directory structure on an **Amazon Linux EC2 instance** using Linux command-line tools.

The objective of this exercise is to simulate a real-world scenario where system administrators must create backups, log backup information, and move backup files for access by other teams.

This lab was performed inside an **AWS EC2 environment** using **SSH and Linux commands**.

---

## Lab Objectives

In this lab, the following tasks were completed:

* Create a backup of an entire directory structure using the `tar` command
* Log backup details including **date, time, and backup filename**
* Move the backup archive to another directory for team access
* Verify the backup file and directory structure

---

## Architecture / Workflow

```
CompanyA Folder Structure
        │
        │
        ▼
Create Backup using tar
        │
        ▼
backup.CompanyA.tar.gz
        │
        ▼
Log Backup Information
(backups.csv)
        │
        ▼
Move Backup File to IA Folder
```

---

## Initial Folder Structure

```
/home/ec2-user/CompanyA
│
├── Employees
│   └── Schedules.csv
│
├── Finance
│   └── Salary.csv
│
├── HR
│   ├── Assessments.csv
│   └── Managers.csv
│
├── IA
│
├── Management
│   ├── Promotions.csv
│   └── Sections.csv
│
└── SharedFolders
```

---

## Step 1 – Connect to EC2 Instance

Connect to the Amazon Linux EC2 instance using SSH.

```bash
chmod 400 labsuser.pem
ssh -i labsuser.pem ec2-user@<Public-IP>
```

---

## Step 2 – Verify Folder Structure

Check the working directory and folder structure.

```bash
pwd
ls -R CompanyA
```

Expected working directory:

```
/home/ec2-user
```

---

## Step 3 – Create Backup Using tar

Create a compressed backup archive of the entire **CompanyA** folder.

```bash
tar -csvpzf backup.CompanyA.tar.gz CompanyA
```

Explanation of options:

| Option | Description              |
| ------ | ------------------------ |
| c      | create archive           |
| v      | verbose output           |
| p      | preserve permissions     |
| z      | gzip compression         |
| f      | specify archive filename |

Verify the backup file:

```bash
ls
```

Output:

```
backup.CompanyA.tar.gz
CompanyA
```

---

## Step 4 – Log Backup Details

Navigate to the CompanyA directory.

```bash
cd /home/ec2-user/CompanyA
```

Create a log file.

```bash
touch SharedFolders/backups.csv
```

Record backup details.

```bash
echo "25 Aug 2021, 16:59, backup.CompanyA.tar.gz" | sudo tee SharedFolders/backups.csv
```

View log file contents:

```bash
cat SharedFolders/backups.csv
```

Output:

```
25 Aug 2021, 16:59, backup.CompanyA.tar.gz
```

---

## Step 5 – Move Backup File

Move the backup archive to the **IA directory**.

```bash
mv ../backup.CompanyA.tar.gz IA/
```

Verify the move:

```bash
ls . IA
```

Output:

```
IA:
backup.CompanyA.tar.gz
```

---

## Key Linux Commands Used

| Command | Purpose                                |
| ------- | -------------------------------------- |
| `tar`   | Create compressed archive backups      |
| `mv`    | Move files between directories         |
| `ls`    | List directory contents                |
| `pwd`   | Display current directory              |
| `echo`  | Print text output                      |
| `tee`   | Write output to both terminal and file |
| `cat`   | Display file contents                  |

---

## Real World Use Case

System administrators often create automated backups of important application folders or data directories. These backups are stored as compressed archives and logged to track when backups were created.

This practice helps:

* Prevent data loss
* Maintain backup history
* Support disaster recovery
* Enable team access to shared backups

---

## Technologies Used

* AWS EC2
* Amazon Linux
* SSH
* Linux CLI
* tar backup utility

---

## Author

**Venkata Tapaswini Nallana**

Cloud • QA • Linux • AWS Projects
