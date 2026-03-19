# AWS Networking Lab – Public vs Private IP Addresses

## Overview

In this lab, I investigated a networking issue involving two EC2 instances inside a Virtual Private Cloud (VPC). One instance could access the internet while the other could not.

The goal of this lab was to understand the difference between **public and private IP addresses** and troubleshoot connectivity issues.

---

## Architecture

Components used in this lab:

- Amazon VPC (CIDR: 10.0.0.0/16)
- Public Subnet
- Internet Gateway
- Two Amazon EC2 Instances
  - Instance A
  - Instance B

Architecture Flow

EC2 Instance → Subnet → Route Table → Internet Gateway → Internet

---

## Problem

Customer issue:

Instance A cannot reach the internet while Instance B can, even though both instances are in the same VPC and subnet.

---

## Investigation

Steps performed:

1. Open AWS EC2 Dashboard
2. Inspect networking configuration of both instances
3. Compare public and private IP addresses
4. Attempt SSH connection to both instances

---

## Findings

Instance A

- Private IP only
- No public IP assigned
- Cannot be accessed from the internet

Instance B

- Private IP
- Public IP assigned
- Accessible from the internet via SSH

---

## Root Cause

Instance A does not have a **public IP address** assigned.

Private IP addresses are only reachable inside the VPC network.

Public IP addresses allow communication with the internet through the Internet Gateway.

---

## Solution

Assign a **public IP address** to the EC2 instance or launch the instance with auto-assign public IP enabled.

---

## Important Concept

AWS VPC networks should use **private IP ranges defined by RFC1918**

Recommended CIDR ranges:

- 10.0.0.0/8
- 172.16.0.0/12
- 192.168.0.0/16

Using public IP ranges (example: 12.0.0.0/16) inside a VPC can cause routing conflicts and connectivity issues.

---

## Skills Demonstrated

- AWS VPC networking
- EC2 instance configuration
- Public vs Private IP understanding
- SSH connectivity
- Cloud troubleshooting methodology

---

## Video Demonstration

YouTube Lab Recording

(Link here after upload)

---

## AWS Services Used

- Amazon EC2
- Amazon VPC
- Internet Gateway