# AWS CloudFormation Automation Lab

This project demonstrates how to deploy AWS infrastructure using Infrastructure as Code (IaC) with AWS CloudFormation.

## Lab Objectives

This lab demonstrates how to:

• Deploy infrastructure using CloudFormation templates  
• Update existing stacks to add new resources  
• Use parameterized templates  
• Automatically manage infrastructure lifecycle  

---

## Architecture

CloudFormation Template

Creates the following resources:

VPC  
Security Group  
S3 Bucket  
EC2 Instance

Workflow:

CloudFormation Template (YAML)
        ↓
Create Stack
        ↓
Deploy VPC + Security Group
        ↓
Update Stack → Add S3 Bucket
        ↓
Update Stack → Add EC2 Instance
        ↓
Delete Stack

---

## Resources Created

• Amazon VPC  
• Security Group  
• Amazon S3 Bucket  
• Amazon EC2 Instance  

---

## Key Concepts

Infrastructure as Code (IaC)

CloudFormation allows infrastructure to be defined as code using YAML or JSON templates.

Reusable Templates

Infrastructure can be deployed consistently across environments.

Automated Resource Management

CloudFormation manages creation, updates, and deletion of resources.

---

## Files in this Repository

task1.yaml → Initial CloudFormation template  
commands.txt → YAML snippets used in the lab  
README.md → Project documentation  

---

## Author

Venkata Tapaswini Nallana
AWS re/Start | Cloud & DevOps Learner