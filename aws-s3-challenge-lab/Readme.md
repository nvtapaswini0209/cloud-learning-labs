# 🚀 AWS S3 Static Website Hosting (Challenge Lab)

## 📌 Project Overview
This project demonstrates how to create an Amazon S3 bucket, upload files, configure permissions, and make content publicly accessible via a web browser using AWS CLI.

---

## 🎯 Objectives
- Create an S3 bucket
- Upload an object (index.html)
- Configure permissions (ACL)
- Access object via browser
- List bucket contents using AWS CLI

---

## 🛠️ Technologies Used
- AWS S3
- AWS CLI
- EC2 (CLI Host)
- Linux Commands

---

## ⚙️ Steps Performed

### 1. Configure AWS CLI
```bash
aws configure
2. Create S3 Bucket
aws s3 mb s3://your-bucket-name --region us-west-2
3. Upload File
echo "Hello from S3 Lab" > index.html
aws s3 cp index.html s3://your-bucket-name
4. Make Object Public
aws s3api put-object-acl \
--bucket your-bucket-name \
--key index.html \
--acl public-read
5. Access via Browser
https://your-bucket-name.s3.us-west-2.amazonaws.com/index.html
6. List Bucket Contents
aws s3 ls s3://your-bucket-name
📸 Screenshots

(Add screenshots here)

🚨 Challenges Faced

ACL edit disabled due to "Bucket owner enforced"

Block Public Access restrictions

AccessDenied error during public access

💡 Key Learnings

S3 security layers (ACL, Block Public Access, Bucket Policy)

CLI vs Console operations

Public access configuration

📌 Conclusion

Successfully created and configured an S3 bucket to host a publicly accessible object using AWS CLI.

👩‍💻 Author

Venkata Tapaswini Nallana