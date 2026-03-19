# AWS EC2 Cost Optimization Lab

## Project Overview
This lab demonstrates how to optimize AWS resources to reduce operational costs by removing unnecessary services and resizing EC2 instances.

## Architecture

EC2 (Cafe Web App)
↓
RDS (MariaDB)

## Optimization Steps

1. Connect to EC2 instance using SSH
2. Stop and remove MariaDB database
3. Connect to CLI Host
4. Use AWS CLI to manage EC2 instance
5. Stop EC2 instance
6. Resize instance from t3.small to t3.micro
7. Restart EC2 instance
8. Verify application functionality
9. Estimate cost using AWS Pricing Calculator

## Tools Used

AWS EC2  
AWS CLI  
Amazon RDS  
AWS Pricing Calculator  
Linux SSH  

## Cost Comparison

Before Optimization:
EC2 (t3.small) + 40GB EBS
Monthly Cost: $35.60

After Optimization:
EC2 (t3.micro) + 20GB EBS
Monthly Cost: $25.18

Estimated Savings:
$10.42 per month

## Key Learning

• Cloud cost optimization  
• AWS CLI instance management  
• Removing unused resources  
• Estimating AWS service pricing