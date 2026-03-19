# AWS VPC Project – Public & Private Subnet Architecture

## 📌 Project Overview
This project demonstrates how to build a secure and scalable AWS network using:
- VPC
- Public and Private Subnets
- Internet Gateway
- NAT Gateway
- Bastion Host
- EC2 Instances

## 🧠 Architecture
- Public Subnet → Internet access via Internet Gateway
- Private Subnet → Outbound access via NAT Gateway
- Bastion Host → Secure SSH access to private instance

## ⚙️ Services Used
- Amazon VPC
- Amazon EC2
- Internet Gateway
- NAT Gateway
- Route Tables

## 🚀 Steps Performed
1. Created VPC with CIDR 10.0.0.0/16
2. Created Public and Private Subnets
3. Configured Internet Gateway
4. Configured Route Tables
5. Launched Bastion Server in Public Subnet
6. Created NAT Gateway
7. Configured Private Route Table with NAT
8. Launched EC2 in Private Subnet
9. Connected via Bastion Host
10. Verified internet using curl and yum

## 🔐 Key Learning
- Private instances cannot access internet directly
- NAT Gateway allows outbound internet access
- Bastion host is used for secure SSH access

## 🧪 Verification
- curl https://amazon.com → SUCCESS
- yum update → SUCCESS

## 📸 Screenshots
See `/screenshots` folder

## 📺 Demo Video
(Attach your YouTube link here)

## 💡 Author
Venkata Tapaswini Nallana