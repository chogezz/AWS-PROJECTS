# **AWS Projects Portfolio**

Welcome to my AWS Projects Portfolio! This repository is a showcase of my proficiency in leveraging various AWS services.

---


## **About Me**

I'm **Noel Choge**, and I'm passionate about emerging technologies specifically in the Cloud.

---

## **Projects**
---

## **Project 1: S3 Static Website**

**Description:**  
Hosting a static website on AWS S3. This project demonstrates the use of AWS services to host a simple, fast-loading website.

**Services Used:**  
- **AWS S3**: For hosting static files.  

**Key Features:**  
- Serverless architecture for high availability and cost efficiency.  
- Simple configuration for hosting static content such as HTML, CSS, and JavaScript files.
- Ideal for application in single page websites such as landing pages for marketing campaigns or service businesses.

---

## **Project 2:Launch EC2 Instance**

**Description:**
Launching an EC2 instance on a public subnet accessible over the internet via ssh.

**Services Used:**
- **AWS EC2**: Launch EC2 instances in the cloud.
- **AWS VPC**: Where EC2 instances are launched.A VPC is a logically isolated network where AWS resources are launched.In this case a public subnet within the VPC is where the EC2 instance is placed so as to access resources from the internet
-  **Internet Gateway**: Attached to the VPC to provide internet access to instances in the public subnet
-  **Security Groups**: A virtual firewall to protect inbound and outbound traffic to the EC2 instance.In this case I allowed all inbound ssh(port 22) traffic for ssh access and all outbound traffic to any destination for internet access.
-  **Key Pairs**: I created a new ssh key pair.It contains a public key which is stored on AWS and a private key which is downloaded to my computer and it is used when connecting to EC2 instance via ssh.

**Key Features:**
- Easy internet access as the public ip and internet gateway offer direct access.
- Customisable resources which offers flexibility.
--- 
---
