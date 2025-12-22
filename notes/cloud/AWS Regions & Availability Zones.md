☁️ **AWS Regions \& Availability Zones**



🔹 What is an AWS Region?



An AWS Region is a geographical location where AWS has multiple data centers.



Examples: Asia Pacific (Mumbai), US East (N. Virginia), Europe (Frankfurt)



Key Points:



Each Region is independent



Data is stored within the chosen Region



You choose a Region based on: Latency, Compliance , Cost, User location



🔹 What is an Availability Zone (AZ)?



An Availability Zone is a physically separate data center within a Region.



Each Region has multiple AZs (usually 2–6)



AZs are connected with high-speed, low-latency networks



Example:



Mumbai Region



ap-south-1a



ap-south-1b



ap-south-1c



🔹 Why Regions \& AZs are Important?



High Availability – If one AZ fails, others continue



Fault Tolerance – Protects against hardware failures



Scalability – Applications can scale across AZs



🔐 AWS IAM (Identity and Access Management)



🔹 What is IAM?



IAM is an AWS service that allows you to securely manage access to AWS resources.



It answers:



Who can access AWS?



What actions they can perform?



Which resources they can access?



🔹 Root User



Created when AWS account is created



Has full, unrestricted access



Should be used only for setup



Best Practice:



❌ Do NOT use root user daily

✅ Enable MFA and lock it away



🔹 IAM User



An IAM User represents a person or application that interacts with AWS.



Features:



Has specific permissions



Can log in to AWS Console or use CLI



Safer than root user



🔹 IAM Groups



A Group is a collection of IAM users.



Why Groups?



Easier permission management



Apply policy once → affects all users



Example:



Admins group



Developers group



🔹 IAM Policies



A Policy defines permissions.



Written in:



JSON format



Example permissions:



Allow EC2 access



Deny S3 deletion



Read-only access



Policies define:



Actions (what)



Resources (where)



Effect (allow/deny)



🔹 IAM Roles (Basic Idea)



An IAM Role is used by AWS services (like EC2, Lambda) to get permissions without passwords.



Example: EC2 role to access S3

(You’ll use this later — just understand the idea now)



🔒 IAM Best Practices



Enable MFA on root account



Use IAM users for daily work



Follow least privilege principle



Never share credentials

