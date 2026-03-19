# 🔐 Amazon Inspector Lab – Vulnerability Assessment & Remediation

## 📌 Overview
This project demonstrates how to use Amazon Inspector to identify and remediate vulnerabilities in AWS Lambda functions.

## 🎯 Objectives
- Activate Amazon Inspector
- Analyze vulnerability findings
- Fix outdated dependencies
- Verify remediation

## 🏗 Architecture
Lambda Function → Amazon Inspector → Findings → Fix → Rescan

## ⚙️ Services Used
- AWS Lambda
- Amazon Inspector
- NVD (National Vulnerability Database)

## 🧪 Vulnerability Found
- CVE-2023-32681
- Package: requests==2.20.0

## 🛠 Fix Applied
Updated:
requests==2.20.0 → requests

## ✅ Result
- Vulnerability status changed from Active → Closed
- Lambda function rescanned successfully

## 🌍 Real-World Use Case
- Secure serverless applications
- Automated vulnerability scanning
- DevSecOps pipelines

## 📺 Demo Video
(YouTube Link Here)

## 📸 Screenshots to Include
- Inspector Activation
- Findings Dashboard
- CVE Details
- Lambda Code Fix
- Closed Findings
