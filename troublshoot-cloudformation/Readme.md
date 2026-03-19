# AWS CloudFormation Troubleshooting Lab

This project demonstrates how to troubleshoot a failed AWS CloudFormation deployment using the AWS CLI.

## Architecture

The CloudFormation template creates:

- VPC
- Public Subnet
- EC2 Web Server
- Security Group
- WaitCondition
- S3 Bucket

## Objectives

- Deploy infrastructure using Infrastructure as Code
- Identify stack creation failures
- Analyze EC2 logs
- Detect configuration drift
- Delete stacks while retaining resources

## Key Concepts

CloudFormation
Infrastructure as Code
Stack Events
Drift Detection
WaitCondition
UserData debugging

## Commands

All CLI commands used in this lab are stored in `commands.txt`.

## Result

Successfully deployed a web server using CloudFormation and resolved deployment issues by analyzing logs and updating the template.

## Screenshots

Recommended screenshots:

- Stack creation
- Stack failure
- EC2 logs
- Drift detection
- Web server output