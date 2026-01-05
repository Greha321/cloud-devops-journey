☁️ Amazon EC2 – Notes

🔹 **What is EC2?**



EC2 (Elastic Compute Cloud) is a service that provides virtual servers in the cloud.



👉 It allows users to create, start, stop, and manage servers on demand.

👉 No physical hardware is required.



🔹**Why it is needed ?**



Traditional servers: Expensive hardware, Slow scaling, Maintenance issues



EC2 solves this by:



Renting servers instead of buying



Scaling in minutes



Paying only for usage



🔹 **EC2 Instance**



An EC2 instance is a running virtual machine.



Instance States:



Running → Server is active



Stopped → Server off (no compute cost)



Terminated → Server deleted permanently



🔹 **AMI (Amazon Machine Image)**



An AMI is a template used to launch EC2 instances.



It includes:



Operating System



Pre-installed software (optional)



Examples:



Amazon Linux 2, Ubuntu, Windows Server



📌 AMI decides which OS the instance runs.



🔹 **Instance Type**



Defines the hardware configuration of EC2.



It controls: CPU, RAM, Network capacity



Example:



t2.micro



1 vCPU



1 GB RAM



Free Tier eligible



📌 Instance type decides performance.



🔹 **Key Pair**



A key pair is used for secure authentication.



It has:



Public key → stored by AWS



Private key (.pem) → stored by user



📌 Without the private key, SSH login is not possible.



🔹 **Security Group**



A security group acts as a virtual firewall.



It controls:



Which ports are open



Who can access the instance



Common rules:



SSH → Port 22 (login)



HTTP → Port 80 (web traffic)



📌 Security groups provide network-level security.



🔹 **EC2 Lifecycle**



Launch → Run → Stop → Start → Terminate



Launch: create instance



Stop: pause instance



Terminate: delete instance permanently



🔹 **EC2 Pricing (Basic Idea)**



Pay only when instance is running



Charged per hour/second



Free Tier provides limited usage



📌 Always stop instances when not in use.



🔹 **Real-Life Example**



A website backend runs on EC2:



User sends request



EC2 processes it



Response sent back



Most cloud applications use EC2 behind the scenes.

