# AWS VPC Networking Lab

This project demonstrates how to build a fully functional networking environment in AWS using Amazon VPC.

## Architecture

VPC → Subnet → Internet Gateway → Route Table → Security Group → EC2 Instance

The EC2 instance is able to access the internet after configuring the networking resources.

## VPC Configuration

VPC CIDR: 192.168.0.0/18  
Subnet CIDR: 192.168.1.0/26  

## Resources Created

- Amazon VPC
- Public Subnet
- Internet Gateway
- Route Table
- Network ACL
- Security Group
- EC2 Instance

## Steps

1. Create VPC
2. Create Public Subnet
3. Create Internet Gateway
4. Attach IGW to VPC
5. Create Route Table
6. Add route 0.0.0.0/0 → IGW
7. Associate subnet with route table
8. Configure Network ACL rules
9. Create Security Group
10. Launch EC2 Instance
11. SSH into instance
12. Test internet connectivity

## Test

Internet connectivity was verified using:

ping google.com

Result: Successful replies with 0% packet loss.

## Outcome

The EC2 instance successfully connects to the internet through the configured VPC networking resources.

## Lab Duration

~60 minutes

## Author

Venkata Tapaswini Nallana