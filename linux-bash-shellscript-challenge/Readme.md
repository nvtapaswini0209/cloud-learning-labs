# AWS Bash Shell Scripting Lab (EC2)

## Project Overview

In this lab, I connected to an Amazon EC2 Linux instance using SSH and created a Bash automation script.

The script automatically generates batches of files while detecting the last created file number.

Each time the script runs, it creates the next 25 files without hardcoding numbers.

This demonstrates basic Linux automation skills commonly used in DevOps and Cloud environments.

---

## Technologies Used

- AWS EC2
- Linux (Amazon Linux)
- SSH
- Bash Scripting

---

## Architecture

Local Machine
      ↓
SSH Connection
      ↓
Amazon EC2 Linux Instance
      ↓
Bash Script Automation
      ↓
File Creation in Directory

---

## Script Functionality

The Bash script performs the following tasks:

1. Detects the last existing file number
2. Calculates the next starting number
3. Automatically creates 25 new files
4. Ensures numbers continue sequentially

Example:

First run:


tapaswini1
tapaswini2
...
tapaswini25


Second run:


tapaswini26
tapaswini27
...
tapaswini50


---

## Bash Script

```bash
#!/bin/bash

name="tapaswini"

last=$(ls $name* 2>/dev/null | sed 's/[^0-9]*//g' | sort -n | tail -1)

if [ -z "$last" ]
then
start=1
else
start=$((last+1))
fi

end=$((start+24))

for i in $(seq $start $end)
do
touch ${name}${i}
done

echo "Created files from ${name}${start} to ${name}${end}"
How to Run the Script

Connect to EC2 via SSH

ssh -i labsuser.pem ec2-user@PUBLIC-IP

Create working directory

mkdir bash-lab
cd bash-lab

Create the script

nano create_files.sh

Make executable

chmod +x create_files.sh

Run the script

./create_files.sh
Verification

Display directory contents

ls -l

The script should create 25 files each time it runs.

Learning Outcome

This lab helped me practice:

Linux command line

Bash scripting automation

Working with EC2 instances

SSH connectivity

File management in Linux

Video Demonstration

YouTube Lab Recording:

(Add your video link here)

Author

Venkata Tapaswini Nallana