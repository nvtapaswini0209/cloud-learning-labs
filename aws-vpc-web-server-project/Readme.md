# AWS VPC + Web Server Project

## 📌 Overview
This project demonstrates how to build a custom Virtual Private Cloud (VPC) and deploy a web server using Amazon EC2.

---

## 🏗️ Architecture

VPC (10.0.0.0/16)
│
├── Public Subnet (10.0.0.0/24)
├── Public Subnet 2 (10.0.2.0/24)
│
├── Private Subnet (10.0.1.0/24)
├── Private Subnet 2 (10.0.3.0/24)
│
├── Internet Gateway
├── NAT Gateway
│
└── EC2 Instance (Web Server)

---

## ⚙️ Services Used

- Amazon VPC
- Amazon EC2
- Security Groups
- Route Tables
- NAT Gateway

---

## 🚀 Steps Performed

1. Created a custom VPC
2. Configured public and private subnets
3. Associated route tables
4. Created a security group for HTTP access
5. Launched EC2 instance
6. Installed Apache Web Server using user data
7. Verified the website via public DNS

---

## 🧠 Key Learnings

- Difference between public and private subnets
- How routing works in AWS
- Security group configuration
- EC2 bootstrapping using user data

---

## 🌐 Output

A working web server hosted on AWS EC2 accessible via public internet.

---

## 📷 Screenshots

(Add your screenshots here)

---

## 🎥 Demo Video

(Add your YouTube link here)