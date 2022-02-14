Part 1:

1. Create VPC
VPC stands for Virtual Private Cloud. It is the virtual network for AWS account, aka netwroking layer for Amazon EC2. A user can have multiple VPC's on one account. It serves as a secure, isolated, private cloud hosted within in a public cloud. You can run code, store data, and host websites. However, private cloud is hosted remotely by a public cloud provider.

2. Create Subnet
Subnet is the range of IP addresses in the VPC. There are two types of subnets, public and private. The public subnet mus be connected to internet for resources. The private subnet will not be connected to internet for resources. ACL and security group can be used to protect AWS resources in subnet. In the subnet, /16 is the largest range while /28 is the smallest range.
 
3. Create Internet Gateway
Internet Gateway is a gateway to attach to the VPC to enable communication between resource in your VPC and internet. Provides a target in your VPC route tables for internet-routable traffic, and NAT for instances which have assigned IPV4 addresses. 

4. Create Route Table
Route tables are set of rules which are also known as routes. These set of rules determine where network traffic is directed. Each route defines range of IP addresses where you want the traffic to traffic (the target/destination). Need a route for traffic within a subnet (other machines on your network). Need a route for traffic to the whole internet (other machines in the world). You can also associate a subnet with route table and if not then it is associated with main route table. 

5. Create Security Group
Securiy Group is a firewall at a network level. This works inside and outside of the VPC. Through this we can allow rules which are inbound and outbound. Acts as a virtual Firewall for EC2 instances to control inbound and outbound traffic

Part 2:
1. I clicked on launch instances and chose an AMI which was Ubuntu Server 20.04 LTS (HVM), SSD Volumr Type 64 bit (x86) Instance type was t2.micro was selected from t2 family which has a low to moderate network performance. I chosse this instance because it is free which read 'free tier eligible'. 
2. I attached it to my VPC by selecting my specific VPC which I made for this project. 
3. I determined that I will disable the auto-assign option for the Public IPv4 address. I did this because i will seperately create an elastic IP and assign it to be attached to this instance. 
4. When attaching a volume to my instance, I chose the option of the general purpose SSD (gp2) which had the volume type of root and size of 16 GiB because I think it is a safe enough size for me to be able to install other softwares while having this to work with. Also, If i chose a size of about 4 GiB this would end up taking the most storage and will not be safe for me. 
5. I added a tag with my name and the name of the instance called 'Qureshi-Ubuntu20.04'. I did this through the step 5 of the isntance launching process. The key was the 'name' while the value was the name of my name 'Qureshi-Ubuntu20.04'.
6. In the configure security group, I associated my security group thorugh the existing security group option. My security group is named Qureshi-sg and I also checked the inbound rules that i created which were displated at the bottom. 
7. When choosing a key pair option, the cons to proceeding without a key pair is that it cant connect. I only connect to these instances with this system only by default. I can create a new key pair but I will have to download it at a safe place and remember it becuase I can only it that specific key to unlock this istance. However, I chose existing key which was vockey and I know i can connect to systems with this key and permissions are already set for it and location is known. I checked off the acknowledgement as well. I then navigated to the elastic Ip option from the network and security option from the side bar and clicked on the 'allocate elastic IP address' button. The network border group was set to us-east-1 and since I forgot to add a tag. I clicked on the allocate button and when it was created I went into the tags section under the description bar at the bottom and added the tag for it which had my name as 'Qureshi-EIP'. and saved the tag. To associate the EIP, I clicked on the actions dropdown and selected associate EIP and then filled out the information. For the resource type, I selected the instance option and then selected my instance which i created which was named Qureshi-Ubuntu20.04, and then selected the Private IP address from the dropdown which only had one option of the IP address which i had and i selected that which was 10.0.0.9 and associated it. I made sure I managed my tag and added name as the key and value as 'Qureshi-EIP'. 
8. Headed to the instance page and refreshed and saw i had a EIP for it and took a screenshot.
9. I inserted the command 'ssh -i /home/marwaq/keys/ceg3120-aws-vm.pem ubuntu@52.71.181.24' then typed yes to what the system asked me and everything was set up. I checked a couple types and everything worked smoothly. Now for the hostname change, I ran the command sudo hostnamectl set-hostname Qureshi-AMI. Then exit and log back in to see the changed hostname.
10. Screenshots taken and stored in Screenshots directory for Part1 and Part2  
