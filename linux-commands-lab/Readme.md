Working with Linux Commands on AWS EC2
Lab Overview

This lab demonstrates how to use essential Linux command-line tools on an Amazon EC2 instance. These commands help manipulate files, process text, and automate tasks in Linux environments commonly used in cloud infrastructure and DevOps workflows.

The lab was performed on an Amazon Linux EC2 t3.micro instance using SSH access.

Objectives

In this lab I practiced the following Linux commands:

tee – Write command output to both terminal and file

sort – Organize data in files

cut – Extract specific columns from text files

sed – Replace or modify text inside files

pipe (|) – Pass output from one command to another

Architecture / Workflow

EC2 Instance
↓
SSH Connection
↓
Linux Terminal Commands
↓
File Manipulation and Output Processing

Task 1 — Connect to EC2 using SSH

Connected to the Amazon Linux EC2 instance using the key pair provided by the AWS lab environment.

Command used
ssh -i labsuser.pem ec2-user@<public-ip>

After connecting successfully, the terminal shows:

[ec2-user@ip-xx-xx-xx-xx ~]$

This confirms access to the EC2 Linux environment.

Task 2 — Using the tee Command

The tee command allows output to be displayed in the terminal and saved into a file simultaneously.

Command
hostname | tee file1.txt
Explanation

hostname prints the system hostname

tee saves the output into file1.txt

Output is also displayed on the terminal

Verify file creation
ls
Task 3 — Using sort and Pipe Operator

Created a CSV file and sorted the data.

Create CSV file
cat > test.csv

Example data:

Factory, 1, Paris
Store, 2, Dubai
Factory, 3, Brasilia
Store, 4, Algiers
Factory, 5, Tokyo

Exit with:

CTRL + D
Sort file contents
sort test.csv

Output becomes alphabetically ordered.

Search using pipe operator
grep Paris test.csv

This filters the result and displays only the line containing Paris.

Task 4 — Using the cut Command

The cut command extracts specific columns from text files.

Create file
cat > cities.csv

Example data:

Dallas, Texas
Seattle, Washington
Los Angeles, California
Atlanta, Georgia
New York, New York
Extract first column
cut -d ',' -f 1 cities.csv
Explanation

-d ',' sets comma as delimiter

-f 1 selects the first field

Output:

Dallas
Seattle
Los Angeles
Atlanta
New York
Task 5 — Using sed Command

The sed command is used to replace or edit text inside files.

Replace first comma with period
sed 's/,/./' cities.csv

Output:

Dallas. Texas
Seattle. Washington
Los Angeles. California
Atlanta. Georgia
New York. New York
Apply to second file
sed 's/,/./' test.csv

Output:

Factory. 1, Paris
Store. 2, Dubai
Factory. 3, Brasilia
Store. 4, Algiers
Factory. 5, Tokyo
Commands Used in This Lab
pwd
hostname | tee file1.txt
ls
cat > test.csv
sort test.csv
grep Paris test.csv
cat > cities.csv
cut -d ',' -f 1 cities.csv
sed 's/,/./' cities.csv
sed 's/,/./' test.csv
Real World Use Cases

These Linux commands are widely used in cloud engineering and DevOps environments:

Command	Real-world use
tee	Logging output during scripts
sort	Organizing logs and datasets
cut	Extracting fields from CSV or logs
sed	Automating configuration edits
pipe	Building command pipelines

These tools are commonly used when managing servers, logs, and automation scripts in AWS EC2 environments.

AWS Resources Used

Amazon EC2

Amazon Linux AMI

SSH

Instance type used:

t3.micro

Resources:
1 vCPU
1 GiB memory

Repository Structure
working-with-linux-commands
│
├── README.md
├── commands-used.txt
├── screenshots
└── videos
Author

Venkata Tapaswini Nallana

AWS Cloud & QA Enthusiast
Focused on Cloud Infrastructure, Linux, and DevOps Learning.