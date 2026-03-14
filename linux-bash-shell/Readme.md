# AWS Linux Bash Shell Lab

## Overview
This lab demonstrates how to work with the Bash shell on an Amazon EC2 instance.  
It focuses on creating command aliases for backup operations and modifying the PATH environment variable to execute scripts from custom directories.

## Objectives
- Connect to an EC2 instance using SSH
- Create a Bash alias for folder backups
- Use the `tar` command to archive directories
- Explore and modify the PATH environment variable
- Execute shell scripts from custom directories

## AWS Services Used
- Amazon EC2
- Amazon Linux

## Instance Details
Instance Type: t3.micro  
Operating System: Amazon Linux

## Lab Tasks

### 1. Connect to EC2 Instance
Connected to an Amazon Linux EC2 instance using SSH.

### 2. Create Backup Alias
Created an alias called `backup` to archive folders using the `tar` command.

Example usage:


backup backup_companyA.tar.gz CompanyA


### 3. Verify Backup
Used `ls` command to verify archive creation.

### 4. Explore PATH Variable
Displayed PATH variable to understand executable search locations.


echo $PATH


### 5. Add Custom Directory to PATH
Added `/home/ec2-user/CompanyA/bin` to the PATH variable.


PATH=$PATH:/home/ec2-user/CompanyA/bin


### 6. Execute Script from PATH
Successfully executed `hello.sh` without specifying full path.


hello.sh


## Key Concepts Learned
- Bash aliases
- Linux archive tools (`tar`)
- Environment variables
- PATH configuration
- Shell script execution

## Demo Video
YouTube Demo (Private or Public):  
Add your link here

## Screenshots
See `/screenshots` folder for step-by-step execution images.

## Author
Venkata Tapaswini Nallana  
Cloud & QA Professional