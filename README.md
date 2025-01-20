# # **AWS Projects Portfolio**

Welcome to my AWS Projects Portfolio! This repository is a showcase of my proficiency in leveraging various AWS services.

---

## **About Me**

I'm **Noel Choge**, and I'm passionate about emerging technologies, specifically in the Cloud.

---

## **Projects**

### **Project 1: S3 Static Website**

**Description:**  
Hosting a static website on AWS S3. This project demonstrates the use of AWS services to host a simple, fast-loading website.

**Services Used:**  
- **AWS S3**: For hosting static files.  

**Key Features:**  
- Serverless architecture for high availability and cost efficiency.  
- Simple configuration for hosting static content such as HTML, CSS, and JavaScript files.  
- Ideal for single-page websites like landing pages for marketing campaigns or service businesses.

---

### **Project 2: Launch EC2 Instance**

**Description:**  
Launching an EC2 instance on a public subnet accessible over the internet via SSH.

**Services Used:**  
- **AWS EC2**: Launch instances in the cloud.  
- **AWS VPC**: A logically isolated network for launching AWS resources. In this project, a public subnet within the VPC is used to ensure internet access.  
- **Internet Gateway**: Provides internet access for instances in the public subnet.  
- **Security Groups**: Acts as a virtual firewall to protect inbound and outbound traffic. In this project, inbound SSH (port 22) traffic is allowed, along with all outbound traffic.  
- **Key Pairs**: A new SSH key pair was created to securely connect to the EC2 instance.  

**Key Features:**  
- Easy internet access with public IP and Internet Gateway.  
- Customizable resources for enhanced flexibility.

---

### **Project 3: HTTP Application Load Balancer Setup**

**Description:**  
Configuring an **Application Load Balancer (ALB)** to distribute traffic across two web servers in different Availability Zones, ensuring high availability and redundancy.

**Steps to Implement:**  
1. **Create a VPC**: Name: `lab-005`, CIDR Block: `192.168.0.0/16`.  
2. **Create Subnets**: Two subnets in different Availability Zones with Auto-assign IPv4 enabled.  
3. **Internet Gateway**: Attach to `lab-005` VPC.  
4. **Modify Route Table**: Add default route to Internet Gateway and associate with both subnets.  
5. **Launch EC2 Instances**: Two `t2.micro` instances, allowing SSH and HTTP traffic. Use a startup script for HTTP server installation.  
6. **Create ALB**: Name: `lab-005`, target group: HTTP on Port 80. Add EC2 instances to the target group.  
7. **Testing**: Use the ALB DNS name to verify traffic distribution across instances.

**Outcome:**  
The ALB successfully distributes traffic between two web servers, ensuring high availability and fault tolerance.

**Technologies Used:**  
- **AWS Services**: VPC, Subnets, Internet Gateway, EC2, Application Load Balancer  
- **Instance Type**: t2.micro  
- **Operating System**: Amazon Linux 2  

---

Here's the updated README with "Project 4" included:

---

# Project 4: WordPress Server Deployment on AWS EC2

## Overview

This project demonstrates the process of deploying a WordPress website on AWS EC2 using the WordPress AMI (Amazon Machine Image) for quick and seamless setup. The goal is to create a fully functional WordPress server hosted on AWS, utilizing essential AWS services such as VPC, EC2, and Route Tables.

## Steps Involved

### 1. Creating a VPC
- A custom VPC (`wordpress-vpc`) is created with an IPv4 CIDR block (`192.168.0.0/16`).

### 2. Creating an Internet Gateway
- An Internet Gateway (`wordpress-gateway`) is created and attached to the `wordpress-vpc`.

### 3. Creating a Public Subnet
- A public subnet (`public-subnet`) within the `wordpress-vpc` is created, with an IPv4 CIDR block (`192.168.100.0/24`).
- Auto-assign IPv4 is enabled for the subnet.

### 4. Creating a Route Table
- A route table (`public-route`) is configured to route traffic to the Internet Gateway.

### 5. Associating the Route to the Public Subnet
- The route table (`public-route`) is associated with the public subnet to ensure internet access.

### 6. Launching a WordPress EC2 Instance
- A WordPress EC2 instance is launched using the WordPress AMI from the AWS Marketplace.
- The instance is placed in the public subnet, with a security group allowing HTTP (port 80), HTTPS (port 443), and SSH (port 22) traffic.
- A new key pair is created and downloaded for SSH access.

### 7. Configuring WordPress
- SSH access is used to connect to the EC2 instance.
- The WordPress setup page is accessed via the public IP of the EC2 instance.
- WordPress is configured by providing details like site title, admin username, password, and email address.

### 8. Accessing WordPress
- The WordPress admin dashboard is accessed using the provided credentials to manage and customize the website.

## Technologies Used

- **AWS Services**: 
  - VPC
  - Subnet
  - Internet Gateway
  - EC2

- **Software**:
  - WordPress AMI (pre-configured for WordPress hosting)

- **Operating System**:
  - Included with the WordPress AMI

## Outcome

A fully functional WordPress server is deployed on AWS EC2 using the WordPress AMI, providing a scalable and reliable platform to host dynamic websites with minimal setup.

---

**Author**  
Noel Choge

---
