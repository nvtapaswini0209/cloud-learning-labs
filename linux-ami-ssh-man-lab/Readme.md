Amazon Linux AMI – SSH Access Lab
Overview

This lab demonstrates how to connect to an Amazon Linux EC2 instance using SSH and explore the Linux manual help system using the man command. The lab helps build foundational skills for working with Linux servers in an AWS cloud environment.

Goal

The goal of this lab is to learn how to securely access a Linux-based EC2 instance using SSH and understand how to use Linux manual pages to view command documentation.

AWS Services Used

Amazon EC2

Amazon VPC

Public Subnet

Amazon Linux AMI

Instance Configuration
Configuration	Details
Instance Type	t3.micro
Operating System	Amazon Linux AMI
Access Method	SSH
Network	VPC with Public Subnet
Architecture
User Computer
     │
     │ SSH (Port 22)
     ▼
Internet
     │
     ▼
AWS Region
     │
     ▼
VPC
     │
     ▼
Public Subnet
     │
     ▼
EC2 Instance (Amazon Linux AMI)
Steps Performed

Started the lab environment in AWS.

Opened the AWS Management Console.

Retrieved the public IP and key pair.

Connected to the EC2 instance using SSH.

Used the man command to explore Linux manual pages.

Examined sections such as NAME, SYNOPSIS, and DESCRIPTION.

Commands Used

Connect to the EC2 instance:

ssh -i labsuser.pem ec2-user@<public-ip>

Open the manual page for the man command:

man man

Exit the manual page:

q
Key Concepts Learned

How to connect to a Linux server using SSH

Basics of Amazon Linux AMI

Understanding Linux command documentation

Navigating Linux manual pages

Real-World Use Case

In real cloud environments, engineers connect to EC2 instances using SSH to manage servers, install applications, and troubleshoot issues. Linux manual pages help administrators quickly understand command usage and system operations.

Example:

ssh ec2-user@server-ip
sudo yum install nginx
sudo systemctl start nginx
Screenshots

Screenshots for this lab are included in the screenshots folder.

Examples:

EC2 instance running

SSH connection terminal

Linux man command output

Conclusion

This lab provides a basic understanding of accessing Amazon Linux EC2 instances using SSH and learning Linux commands through the manual help system. These skills are fundamental for cloud engineers, DevOps engineers, and system administrators working with AWS environments.