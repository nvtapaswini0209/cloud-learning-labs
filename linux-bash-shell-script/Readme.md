# Bash Shell Script Backup Automation on AWS EC2

## Project Overview
This lab demonstrates how to automate folder backups on a Linux EC2 instance using a Bash shell script.

The script compresses the **CompanyA** directory and creates a backup archive with the current date.

Example output file:

2026_03_13-backup-CompanyA.tar.gz

---

## AWS Services Used
- Amazon EC2
- Linux (Amazon Linux)
- Bash Shell Scripting

---

## Architecture

Local Machine
     │
     │ SSH
     ▼
Amazon EC2 (Amazon Linux)
     │
     │ Bash Script
     ▼
Compressed Backup Archive (.tar.gz)

---

## Steps Performed

1. Launch Amazon Linux EC2 instance
2. Connect using SSH
3. Create bash script
4. Automate backup using tar command
5. Verify archive creation

---

## Bash Script


Paste script:

#!/bin/bash

DAY="$(date +%Y_%m_%d)"
BACKUP="/home/$USER/backups/$DAY-backup-CompanyA.tar.gz"

tar -csvpzf $BACKUP /home/$USER/CompanyA

Continue README:

---

## Output Verification

Command used:

ls backups/

Example Output:

2026_03_13-backup-CompanyA.tar.gz

---

## Real World Use Case

This automation is commonly used by:

• DevOps Engineers  
• Cloud Engineers  
• System Administrators  

Typical use cases include:

- Automated server backups
- Log archiving
- Disaster recovery preparation
- Scheduled cron backups

---

## Video Demonstration

Full lab walkthrough available on YouTube.

---

## Author

Venkata Tapaswini Nallana
Cloud | QA | AWS Projects