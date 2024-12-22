**A SINGLE EC2 INSTANCE**
---
*Intro*
---

Creating a single EC2 Instance in a public subnet accesible over the internet via SSH.

---
*Steps*
---

*1.Launch EC2 on AWS Console*
---

Select and click launch instance 

Select the appropriate AMI.An AMI is a Software configuration that contains the Operating System,Application Servers and Applications which are required to launch the instance.

*2.Define the Instance Type*
---

The Instance type defines the memory capacity,cpu and architecture that the instance will support

*3.Network Settings*
---

I selected the public default subnet and also enabled the auto-assign public ip function.

*4.Storage Settings*
---

I accepted the default settings which creates an EBS volume

*5.Security Groups*
---

This is a firewall for the instance.I created a security group named ssh-access which has rules that allow ssh from anywhere

*6.Launch Instance*
---

Review all the configurations and launch the instance.

*7.Create a Key Pair*
---

I created a key pair which was then downloaded to my computer directory.
