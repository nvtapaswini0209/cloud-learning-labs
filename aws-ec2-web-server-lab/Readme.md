# AWS EC2 Web Server Lab

## Overview

This project demonstrates how to launch, configure, monitor, and manage a web server using Amazon EC2. The lab focuses on fundamental AWS cloud concepts such as instance creation, networking, security configuration, monitoring, and resource scaling.

## Objective

The goal of this lab is to understand how to deploy and manage a virtual server in the AWS Cloud. It includes launching an EC2 instance, installing a web server, configuring security groups to allow web traffic, monitoring performance, resizing compute and storage resources, and safely terminating the instance.

## AWS Services Used

* Amazon EC2
* Amazon EBS
* Amazon CloudWatch
* Amazon VPC
* Internet Gateway
* Security Groups

## Architecture

User → Internet → Internet Gateway → VPC → EC2 Instance → EBS Storage

Amazon CloudWatch monitors the EC2 instance performance and health.

### Architecture Diagram

![Architecture](architecture/ec2-architecture.png)

## Key Tasks Performed

* Launched an EC2 instance using Amazon Linux AMI
* Selected instance type and configured storage
* Created and configured a security group to allow HTTP access
* Installed and ran Apache web server using a user data script
* Accessed the web server using the instance public IP address
* Monitored instance metrics using CloudWatch
* Resized the EC2 instance and increased EBS storage
* Enabled and tested termination protection
* Terminated the EC2 instance after completing the lab

## Screenshots

### EC2 Instance Running

![EC2 Instance](screenshots/ec2-instance-running.png)

### Security Group Configuration

![Security Group](screenshots/security-group-http.png)

### Web Server Output

![Web Server](screenshots/web-server-output.png)

### CloudWatch Monitoring

![CloudWatch](screenshots/cloudwatch-monitoring.png)

## Folder Structure

```
2. aws-ec2-web-server-lab
│
├── README.md
├── architecture
│   └── ec2-architecture.png
│
└── screenshots
    ├── ec2-instance-running.png
    ├── security-group-http.png
    ├── web-server-output.png
    └── cloudwatch-monitoring.png
```

## What I Learned

* How to deploy and configure a cloud server using EC2
* How to manage the EC2 instance lifecycle
* How to configure security groups to control network access
* How to monitor infrastructure using CloudWatch
* How to scale compute and storage resources in AWS

## Author

Venkata Tapaswini Nallana
