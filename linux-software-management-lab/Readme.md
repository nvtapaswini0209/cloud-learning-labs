# AWS Linux Software Management Lab

## Overview
In this lab, I practiced Linux software management on an Amazon EC2 instance.  
The lab demonstrates how to update system packages, roll back package changes, install the AWS CLI, and interact with AWS services from the command line.

This lab was performed in an AWS sandbox environment.

---

## Technologies Used
- Amazon EC2
- Amazon Linux
- YUM Package Manager
- AWS CLI
- SSH
- Linux Terminal

---

## Objectives

- Connect to an EC2 instance using SSH
- Update Linux packages using YUM
- View package history
- Roll back package updates
- Install AWS CLI
- Configure AWS CLI
- Retrieve EC2 instance information using CLI

---

## Lab Architecture

User Computer
↓
SSH Connection
↓
Amazon EC2 Instance (Amazon Linux)
↓
YUM Package Manager
↓
AWS CLI
↓
AWS EC2 API

---

## Steps Performed

### 1. Connect to EC2 via SSH

Connected to the Amazon Linux instance using a key pair.

### 2. Update Linux Packages

Used YUM to check for updates and upgrade installed packages.

### 3. Install Apache Package

Installed the httpd package using YUM.

### 4. View Package History

Used the YUM history command to view package installation history.

### 5. Roll Back Package Transaction

Used YUM rollback functionality to undo a package installation.

### 6. Install AWS CLI

Downloaded and installed AWS CLI v2 using curl and unzip.

### 7. Configure AWS CLI

Configured AWS CLI with region and output format.

### 8. Retrieve EC2 Instance Information

Used AWS CLI to describe EC2 instance attributes.

---

## Screenshots

Screenshots of each step are available in the `screenshots` folder.

---

## Video Demonstration

Full walkthrough video of this lab:

YouTube: *(paste your video link here)*

---

## Key Learning

- Linux package management using YUM
- Managing software updates on cloud servers
- Installing command line tools on EC2
- Interacting with AWS services through AWS CLI
- Basic Linux system administration skills in the cloud

---

## Author

Venkata Tapaswini Nallana  
Cloud & QA Engineer | AWS | Linux | Automation