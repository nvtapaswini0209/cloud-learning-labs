# AWS CloudFormation VPC + EC2 Lab

## Overview
This project demonstrates how to automate AWS infrastructure using **AWS CloudFormation (Infrastructure as Code)**.

The CloudFormation template automatically creates networking and compute resources inside AWS.

Resources created in this lab:

- Amazon VPC
- Internet Gateway
- Private Subnet
- Security Group allowing SSH access
- Amazon EC2 Instance (t3.micro)

The EC2 instance uses the **latest Amazon Linux AMI retrieved automatically from AWS Systems Manager Parameter Store**, which ensures compatibility across AWS regions.

---

## Architecture

CloudFormation Template
        │
        ▼
       VPC
        │
        ▼
Internet Gateway
        │
        ▼
   Private Subnet
        │
        ▼
  Security Group
        │
        ▼
    EC2 Instance

---

## AWS Services Used

| Service | Purpose |
|-------|-------|
| AWS CloudFormation | Infrastructure automation |
| Amazon VPC | Creates isolated virtual network |
| Internet Gateway | Enables internet connectivity |
| Security Group | Controls instance traffic |
| Amazon EC2 | Provides compute resources |
| AWS Systems Manager Parameter Store | Retrieves latest Amazon Linux AMI |

---

## CloudFormation Resources Created

### VPC
CIDR block:

10.0.0.0/16

### Subnet

CIDR block:

10.0.1.0/24

### Security Group

Inbound rule:

Protocol: TCP  
Port: 22  
Source: 0.0.0.0/0

### EC2 Instance

Instance type:

t3.micro

AMI is automatically retrieved using SSM Parameter Store.

---

## Deployment Steps

1. Open **AWS CloudFormation**
2. Click **Create Stack**
3. Upload template file

vpc-ec2-template.yaml

4. Enter stack name

restart-vpc-ec2

5. Review configuration and create stack

6. Wait until stack status shows:

CREATE_COMPLETE

---

## Verification

After deployment verify resources:

VPC → Your VPCs  
EC2 → Instances  
EC2 → Security Groups  
VPC → Subnets

EC2 instance status should show:

Running

---

## Key Learning Outcomes

This lab demonstrates:

- Infrastructure as Code (IaC)
- Automating AWS resource deployment
- Basic AWS networking architecture
- Using CloudFormation templates

---

## Author

Venkata Tapaswini Nallana

AWS re/Start Cloud Computing Student