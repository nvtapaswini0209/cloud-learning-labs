# AWS Lab – Managing Resources with Tagging

This project demonstrates how to manage AWS EC2 instances using resource tags and automation.

## Architecture

Lab VPC
│
├── Public Subnet
│     └── CommandHost (AWS CLI installed)
│
└── Private Subnet
      └── 8 EC2 Instances

## Tags Used

Project
Version
Environment

Example:

Project = ERPSystem
Environment = development
Version = 1.0

## Objectives

• Apply tags to AWS resources
• Find resources using tags
• Modify resource tags using AWS CLI
• Stop and start EC2 instances based on tags
• Implement security policy to terminate untagged instances

## Technologies Used

AWS EC2  
AWS CLI  
JMESPath Query Language  
AWS SDK for PHP  

## Tasks Performed

1. Find instances using AWS CLI
2. Filter instances using JMESPath
3. Update version tags automatically
4. Stop development instances
5. Restart instances
6. Identify instances missing required tags
7. Automatically terminate non-compliant instances

## Learning Outcome

This lab demonstrates how resource tagging can be used for:

• Infrastructure automation
• Environment management
• Security enforcement
• Cost control

## Real-World Use Case

Many organizations shut down development environments after business hours to reduce costs.

Tag-based automation helps companies:

• Control infrastructure
• Reduce cloud costs
• Enforce security policies
• Manage large-scale environments

## Commands Used

See commands.txt