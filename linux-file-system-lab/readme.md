AWS Linux File System Lab (EC2)
Overview

In this lab, I connected to an Amazon EC2 Linux instance using SSH and practiced essential Linux file system operations. The goal of this lab was to learn how to create directories, manage files, copy folders, move directories, and reorganize a folder structure using Linux commands.

This hands-on exercise helps build fundamental skills required for Cloud Support, DevOps, and Cloud Engineering roles.

Lab Environment

Cloud Provider: AWS

Service Used: Amazon EC2

Instance Type: t3.micro

Operating System: Amazon Linux

Connection Method: SSH

User: ec2-user

Architecture / Workflow
Local Machine
     │
     │ SSH
     ▼
Amazon EC2 Instance (Linux)
     │
     │ Linux Commands
     ▼
File System Management
Objectives

In this lab I performed the following tasks:

Connected to an EC2 instance using SSH

Created a directory structure

Created files using Linux commands

Copied directories and files

Moved directories

Deleted files and folders

Reorganized the folder structure

Initial Folder Structure
/home/ec2-user/CompanyA
│
├── Finance
│   ├── Salary.csv
│   └── ProfitAndLossStatements.csv
│
├── HR
│   ├── Assessments.csv
│   └── TrialPeriod.csv
│
└── Management
    ├── Managers.csv
    └── Schedule.csv
Final Folder Structure After Reorganization
/home/ec2-user/CompanyA
│
└── HR
    │
    ├── Finance
    │   ├── Salary.csv
    │   └── ProfitAndLossStatements.csv
    │
    ├── Management
    │   ├── Managers.csv
    │   └── Schedule.csv
    │
    └── Employees
        ├── Assessments.csv
        └── TrialPeriod.csv
Linux Commands Used
Command	Purpose
pwd	Display current directory
ls	List files and folders
mkdir	Create directories
cd	Change directory
touch	Create empty files
cp -r	Copy folders recursively
mv	Move files or folders
rm	Remove files
rmdir	Remove empty directories
ls -laR	List directory contents recursively
Example Commands

Create directories

mkdir CompanyA
cd CompanyA
mkdir Finance HR Management

Create files

touch Salary.csv ProfitAndLossStatements.csv
touch Assessments.csv TrialPeriod.csv

Copy folders

cp -r Finance HR

Move folders

mv Management HR

Delete files

rm Finance/Salary.csv

Remove empty folder

rmdir Finance
Key Learning Outcomes

From this lab I learned:

How to manage files and directories in Linux

How to navigate Linux file systems

How to organize company data structures

How Linux commands are used in real cloud environments

How system administrators manage file systems on EC2 servers

These skills are essential for Cloud Engineers, DevOps Engineers, and System Administrators.

Screenshots

Add screenshots such as:

EC2 SSH connection

Creating directories

File creation

Folder structure verification


Author

Venkata Tapaswini Nallana

Cloud | QA | AWS | Linux | DevOps Learning Journey