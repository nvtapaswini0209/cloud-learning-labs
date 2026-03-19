# AWS Monitoring Infrastructure Lab

## Overview

This project demonstrates how to implement monitoring for AWS infrastructure using Amazon CloudWatch and AWS Config.

Monitoring helps ensure application reliability, detect system issues, and maintain compliance with infrastructure standards.

## Services Used

- Amazon EC2
- Amazon CloudWatch
- CloudWatch Agent
- CloudWatch Logs
- CloudWatch Metrics
- CloudWatch Events
- Amazon SNS
- AWS Systems Manager
- AWS Config

## Architecture

EC2 Web Server  
↓  
CloudWatch Agent  
↓  
CloudWatch Logs + Metrics  
↓  
Metric Filter (404 Errors)  
↓  
CloudWatch Alarm  
↓  
SNS Email Notification  

## Lab Tasks

### 1 Install CloudWatch Agent

Used Systems Manager Run Command to install the CloudWatch agent on the EC2 instance.

### 2 Configure Monitoring

Created a configuration in Systems Manager Parameter Store to collect:

- Web server access logs
- Web server error logs
- CPU metrics
- Disk metrics
- Memory metrics

### 3 Monitor Application Logs

CloudWatch Logs was used to monitor:

- Apache access logs
- Apache error logs

### 4 Create Metric Filter

Created a filter to detect HTTP 404 errors.

### 5 Create Alarm

Configured a CloudWatch alarm to trigger when:

404 errors ≥ 5 in 1 minute

### 6 Configure Notifications

Used Amazon SNS to send email alerts.

### 7 Monitor System Metrics

Observed CPU, disk, and memory metrics using CloudWatch Metrics.

### 8 Real Time Infrastructure Events

Created CloudWatch Event rule to detect:

- EC2 instance stopped
- EC2 instance terminated

### 9 Compliance Monitoring

AWS Config rules were used to detect:

- Resources missing required tags
- Unattached EBS volumes

## Real World Use Case

Organizations use CloudWatch monitoring to:

- Detect application errors
- Monitor infrastructure health
- Receive automated alerts
- Ensure compliance with policies

## Outcome

This lab demonstrates a full monitoring pipeline for AWS infrastructure.