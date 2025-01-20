
---

# AWS Projects Portfolio

Welcome to my **AWS Projects Portfolio**! This repository showcases my proficiency in leveraging various AWS services to build scalable and efficient cloud-based solutions.

---

## About Me

I'm **Noel Choge**, passionate about emerging technologies, especially in Cloud computing. This portfolio highlights the practical experience I’ve gained by working with AWS services.

---

## Projects

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
4. **Modify Route Table**: Add a default route to the Internet Gateway and associate with both subnets.  
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

### **Project 4: WordPress Server Deployment on AWS EC2**

**Description:**  
Deploying a WordPress website on AWS EC2 using the WordPress AMI for a quick and seamless setup. This project creates a fully functional WordPress server hosted on AWS with minimal configuration.

**Steps to Implement:**  
1. **Create a VPC**: A custom VPC (`wordpress-vpc`) with CIDR block `192.168.0.0/16`.  
2. **Create an Internet Gateway**: Attach the Internet Gateway (`wordpress-gateway`) to the VPC.  
3. **Create a Public Subnet**: A subnet (`public-subnet`) with CIDR block `192.168.100.0/24` and enable auto-assign IPv4.  
4. **Create a Route Table**: Add a default route to the Internet Gateway and associate it with the public subnet.  
5. **Launch EC2 Instance**: Launch a WordPress EC2 instance using the WordPress AMI. Assign the instance to the public subnet, with a security group allowing HTTP, HTTPS, and SSH traffic.  
6. **Connect to EC2 Instance**: Use SSH to access the instance and complete the WordPress installation via the public IP.  
7. **Configure WordPress**: Set up site title, admin credentials, and other WordPress settings.  
8. **Access WordPress**: Log in to the WordPress admin dashboard and customize the website.

**Technologies Used:**  
- **AWS Services**: VPC, Subnet, Internet Gateway, EC2  
- **Software**: WordPress AMI (pre-configured for WordPress hosting)  
- **Operating System**: Included with the WordPress AMI  

**Outcome:**  
A fully functional WordPress server deployed on AWS EC2 using the WordPress AMI, providing a reliable and scalable platform for dynamic websites.

---

## Technologies Used

- **AWS Services**: VPC, EC2, S3, Load Balancer, Internet Gateway
- **Software**: WordPress, Amazon Linux 2
- **Operating System**: Managed via AMIs

---

**Author**  
Noel Choge

---
