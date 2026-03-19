# AWS EC2 Static vs Dynamic IP Lab

## Project Overview

This project demonstrates the difference between **dynamic and static IP addresses in AWS EC2** and how to solve an issue where a public IP address changes every time an instance is stopped and started.

In this lab scenario, a customer reported that their EC2 instance public IP address keeps changing, causing their infrastructure to break. As a Cloud Support Engineer, the goal was to investigate the issue and provide a solution.

---

## Problem

The EC2 instance receives a **dynamic public IP address** by default.
When the instance is stopped and started again, AWS assigns a new public IP address.

This causes issues for systems that rely on a **fixed IP address**.

---

## Solution

The issue was resolved by allocating and associating an **Elastic IP (EIP)** with the EC2 instance.

An Elastic IP provides a **persistent public IP address** that remains the same even after the instance is restarted.

---

## AWS Services Used

* Amazon EC2
* Elastic IP
* VPC
* Security Groups

---

## Architecture

VPC
│
├── Public Subnet
│      └── EC2 Instance (Amazon Linux 2)
│             └── Elastic IP (Static Public IP)

---

## Steps Performed

1. Launched an EC2 instance in a public subnet.
2. Observed the public and private IP addresses.
3. Stopped and restarted the instance.
4. Verified that the **public IP address changed**.
5. Allocated an Elastic IP address.
6. Associated the Elastic IP with the EC2 instance.
7. Restarted the instance again to verify the IP remains **static**.

---

## Key Learning

* EC2 public IP addresses are **dynamic by default**
* Private IP addresses remain **persistent**
* Elastic IPs provide **static public IPs**
* Useful for applications that require fixed endpoints

---

## Real-World Use Case

Elastic IP addresses are commonly used for:

* Web servers
* Public APIs
* Bastion hosts
* DNS mapping
* Firewall allowlists

---

## Author

Venkata Tapaswini Nallana
Cloud / QA Engineer
