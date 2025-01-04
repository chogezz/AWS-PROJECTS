**LAUNCH AN EC2 IN A PRIVATE SUBNET AND JUMP HOST**
---
*Intro*
---

Accessing an EC2 Instance whic was launched in a Private Subnet using a Jump Host..

---
*Steps*
---

*1.Creating a VPC*
---

Select create VPC.

Name the VPC lab-002 and assign IPv4 CIDR Block 192.168.0.0/16.

*2.Create Internet Gateway*
---

Create a VPC with the name lab-002 and then attach it to lab-002 VPC

*3.Create a Public Subnet*
---

Create a Public Subnet which is on lab-002 VPC and is named *public* with IPv4 CIDR Block *192.168.100.0/24*.Make sure to enable auto-assign IPv4 in the subnet.

*4.Create a Route Table*
---

Create a Route Table with the name *public* and has a default gateway to the Internet Gateway which was created earlier on in this lab.

*5.Associate the Route to the Public Subnet*
---

Do this by selecting the subnet associations tab then selecting the route created in the previous step.

*6.Create a Private Subnet*
---

The Subnet is on lab-002 VPC and is named *private* with IPv4 CIDR Block *192.168.200.0/24*

*7.Launch 2 Instances*
---

Steps are similar to lab-001(Launch EC2 Instance) then make sure to assign EC2 Instance A to the public subnet and EC2 Instance B to the private subnet.

*8.Open local terminal*
---

- Go to the directory where lab-002 pem file is stored
- Set permissions such that only admin can read the files
- Upload the pem file to the EC2 Instance using scp.
- Connect to EC2 Instance A using ssh.
- ssh into instance B from A using B's Private Address

