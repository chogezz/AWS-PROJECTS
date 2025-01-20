**DEPLOYING A WORDPRESS SERVER ON EC2**

---

**Intro**

Deploying a WordPress server on AWS EC2 using the WordPress AMI for quick and seamless setup.

---

**Steps**

1. **Creating a VPC**
   
   - Select "Create VPC."
   - Name the VPC: `wordpress-vpc` and assign IPv4 CIDR Block: `192.168.0.0/16`.

2. **Create Internet Gateway**
   
   - Name the Internet Gateway: `wordpress-int-gw`.
   - Attach it to the `wordpress-vpc` VPC.

3. **Create a Public Subnet**
   
   - Created a Public Subnet within the `wordpress-vpc` VPC.
   - Named the subnet: `wordpress-subnet`.
   - Assign IPv4 CIDR Block: `192.168.100.0/24`.
   - Enable Auto-assign IPv4 in the subnet.

4. **Create a Route Table**
   
   - Name the Route Table: `public-rt`.
   - Add a default gateway route to the Internet Gateway created earlier.

5. **Associate the Route to the Public Subnet**
   
   - Select the "Subnet Associations" tab.
   - Associate the `public-route` Route Table with the Public Subnet.

6. **Launch a WordPress EC2 Instance**
   
   - Launch an EC2 instance using the **WordPress AMI** from the AWS Marketplace.
   - Assign the instance to the Wordpress Subnet.
   - Configure the security group to allow HTTP (port 80) , and SSH (port 22) traffic.
   - Create and download a new key pair for SSH access.

7. **Configure WordPress**
   
   - Connect to the EC2 instance via SSH:
     ```
     ssh -i "wordpress-sg.pem" ec2-user@44.222.208.236
     ```
   - Access the WordPress setup interface by opening the public IP of the instance in a browser.
   - Complete the WordPress installation process.

8. **Access WordPress**

   - Use the provided admin credentials to log in to the WordPress dashboard.
   - Customize your site as needed.

---

**Outcome**

A fully functional WordPress server is deployed on AWS EC2 using the WordPress AMI, simplifying the process of hosting a dynamic website.

---

**Services Used**
- **AWS Services**: VPC, Subnet, Internet Gateway, EC2
- **Software**: WordPress AMI (pre-configured for WordPress hosting)
- **Operating System**: Included with the WordPress AMI

---

**Author**
**Noel Choge**


