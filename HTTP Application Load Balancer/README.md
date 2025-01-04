**HTTP APPLICATION LOAD BALANCER**
---
*Intro*
---

Illustrating How Application Load Balancer Distributes Traffic Across Two Web Servers Running on Different Availability Zones.

---
*Steps*
---

*1.Creating a VPC*
---

Select create VPC.

Name the VPC: *lab-005* and assign IPv4 CIDR Block: *192.168.0.0/16*.

*2.Create Subnets*
---

Create Two Subnets with each subnet in a different Availability Zone of the VPC.Specify IPv4 CIDR blocks for each subnet according to the diagram.

Ensure both subnets have enabled the auto-assign IPv4 feature

*3.Create an Internet Gateway*
---

Name it *lab-005* and make sure to attach it to lab-005 VPC

*4.Modify the Route Table*
---

Add a default route to the VPC router which has a destination to the Internet Gateway.

Then associate both subnets to the Main route table.

*5.Launch 2 EC2 Instances*
---

Each subnet has an EC2 Instance

Used AMI 2023

Used t2.micro Instance type

Created a new key pair named *lab-005*

Associate each subnet with the lab-005 VPC

Created security groups which allows inbound ssh & http traffic

Used the data script provided to install HTTP server on the instance.


*6.Create an Application Load Balancer*
---

Application load balancer has the name:*lab-005*

Select the Availability Zones and their respective Subnets

Select the security group which was created in the initial steps.

Create a target group with the name: lab-005, Target type: Instance, Protocol:HTTP, Port:80

Add  both instances to the target group which is instance-A and instance-B

Successfully create load balancer

*7.Testing*
---

Copy the dns name associated with the load balancer and paste it on a browser to access it.Both Instances are giving back a response which confirms the load balancer is working

![image](https://github.com/user-attachments/assets/5e101263-452e-44c4-bd69-38bed124684e)
