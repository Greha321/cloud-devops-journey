\# SSH \& Linux Basics (Day 8)



\## What is SSH?

SSH (Secure Shell) is a network protocol used to securely connect to a remote server over the internet.

In AWS, SSH is used to access EC2 instances securely using key pairs instead of passwords.



SSH works on:

\- Port: 22

\- Authentication: Public \& Private key pair



---



\## SSH in AWS EC2



\### Key Concepts

\- \*\*Key Pair\*\*: Used instead of passwords

&nbsp; - `.pem` file → private key (kept secure on local machine)

\- \*\*Username\*\*:

&nbsp; - Amazon Linux → `ec2-user`

\- \*\*Public IPv4\*\*:

&nbsp; - Used to connect from local machine

&nbsp; - Changes if EC2 is stopped \& started



---



\## Steps to Connect to EC2 via SSH (Windows)



1\. Ensure EC2 instance is \*\*running\*\*

2\. Ensure Security Group allows:

&nbsp;  - SSH (port 22) from My IP / Anywhere

3\. Open Command Prompt / PowerShell

4\. Navigate to key file location:

&nbsp;  ```cmd

&nbsp;  cd Downloads

5\. Fix key permissions:

&nbsp;        icacls ec2-key.pem /inheritance:r

&nbsp;        icacls ec2-key.pem /grant:r "%USERNAME%":R

6\. Connect using SSH:

&nbsp;        ssh -i ec2-key.pem ec2-user@<PUBLIC-IP>



7\. Type yes when prompted

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

\## Linux Basics (Inside EC2)

Common Linux Commands Used

**Command**	                **Purpose**

* whoami          Shows current logged-in user
* pwd             Shows current directory
* ls              Lists files and directories
* mkdir demo      Creates a directory
* cd demo 	   Moves into directory
* touch hello.txt 	Creates a file
* ls -l	        Lists files with permissions

\## **File Permissions** (Intro)



Example output:



-rw-r--r-- 1 ec2-user ec2-user hello.txt





Meaning:



rw- → owner can read \& write



r-- → group can read



r-- → others can read



**Why SSH \& Linux Are Important**



Almost all cloud servers run Linux



DevOps engineers manage servers via SSH



Used for:

* Application deployment
* Log analysis
* Server troubleshooting
