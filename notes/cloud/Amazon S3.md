#### ☁️ **Amazon S3** 



🔹 **What is Amazon S3?**



Amazon S3 (Simple Storage Service) is an object storage service used to store and retrieve any amount of data from anywhere.



* Highly scalable
* Highly durable
* Pay-as-you-go



📌 S3 is part of Amazon Web Services (AWS).



🔹 **Key Terminology**

🪣 Bucket



* A bucket is a top-level container in S3.
* Bucket names must be globally unique.
* A bucket is created in a specific region.



📦 Object



An object is a file stored in a bucket.



Consists of:



* Data (file)
* Metadata
* Unique key (object name)



Examples:



* image.jpg
* resume.pdf
* index.html



**🔹 S3 vs EC2 (Important Difference)**



**Feature	           EC2	                  S3**

* Type	         Compute	        Storage
* Used for    Running apps	       Storing files
* OS	           Yes	                  No
* Data	        Temporary	       Persistent

📌 EC2 processes data, S3 stores data.



**🔹 S3 Use Cases**



* Store images, videos, documents
* Application backups
* Log storage
* Static website hosting
* Data for analytics



🔹 **S3 Access \& Permissions (Basic)**



Buckets and objects are private by default



Access controlled using:

* Bucket policies
* IAM policies
* Public access must be explicitly enabled



📌 Never make sensitive data public.



🔹 **Static Website Hosting (Concept)**



S3 can host static websites:



* HTML
* CSS
* JavaScript



No backend code runs on S3.









