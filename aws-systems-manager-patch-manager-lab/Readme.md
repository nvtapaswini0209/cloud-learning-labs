# AWS Systems Hardening using Patch Manager

## 📌 Project Overview
This project demonstrates how to use AWS Systems Manager Patch Manager to automate patching and ensure compliance across EC2 instances.

---

## 🎯 Objectives
- Patch Linux instances using default baseline
- Create custom patch baseline for Windows
- Use patch groups for targeted patching
- Verify patch compliance

---

## 🏗️ Architecture
EC2 Instances
   ↓
Systems Manager
   ↓
Patch Manager
   ↓
Run Command
   ↓
Patch Baseline
   ↓
Compliance Reporting

---

## 🧪 Steps Performed

### 1. Linux Patching
- Used AWS default patch baseline
- Patched instances using tag: LinuxProd

### 2. Custom Patch Baseline
- Created Windows patch baseline
- Configured security updates only

### 3. Patch Group
- Created Patch Group: WindowsProd
- Associated with baseline

### 4. Windows Patching
- Tagged EC2 instances
- Executed patch operation

### 5. Compliance Verification
- Verified all instances are compliant

---

## 📊 Result
- 6 EC2 instances patched successfully
- Compliance status: ✅ Compliant

---

## 📸 Screenshots to Include
- Fleet Manager instances
- Patch baseline creation
- Tagging EC2
- Patch execution status
- Compliance dashboard

---

## 🚀 Real-World Use Case
Used in enterprise environments to:
- Maintain security compliance
- Automate OS patching
- Reduce manual effort
- Improve system reliability

---

## 🧠 Key Concepts
- Patch Baseline
- Patch Groups
- Systems Manager
- Run Command
- Compliance Reporting