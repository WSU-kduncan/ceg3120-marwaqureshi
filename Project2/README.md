Part 1:

1. Create VPC
![CreateVPC](\\wsl.localhost\Ubuntu\home\marwaq\ceg3120-marwaqureshi\Project2\VPC-images) 
![CreateVPC-screenshot](C:\Users\marwa\Desktop\ceg3120\CreateVPC-screenshot.jpg)
![createdvpc](C:\Users\marwa\Desktop\ceg3120\createdvpc.jpg)
![createvpcproof](C:\Users\marwa\Desktop\ceg3120\createvpcproof.jpg)
VPC stands for Virtual Private Cloud. It is the virtual network for AWS account, aka netwroking layer for Amazon EC2. A user can have multiple VPC's on one account. It serves as a secure, isolated, private cloud hosted within in a public cloud. You can run code, store data, and host websites. However, private cloud is hosted remotely by a public cloud provider.

2. Create Subnet
![subnet1](C:\Users\marwa\Desktop\ceg3120\subnet1.jpg)
![subnet-created-successfully](C:\Users\marwa\Desktop\ceg3120\subnet-created-successfully.jpg)
Subnet is the range of IP addresses in the VPC. There are two types of subnets, public and private. The public subnet mus be connected to internet for resources. The private subnet will not be connected to internet for resources. ACL and security group can be used to protect AWS resources in subnet. In the subnet, /16 is the largest range while /28 is the smallest range.
 
3. Create Internet Gateway
![internet-gateway](C:\Users\marwa\Desktop\ceg3120\internet-gateway.jpg)
![internet-gateway-attached-to-VPC](C:\Users\marwa\Desktop\ceg3120\internet-gateway-attached-to-VPC.jpg)
Internet Gateway is a gateway to attach to the VPC to enable communication between resource in your VPC and internet. Provides a target in your VPC route tables for internet-routable traffic, and NAT for instances which have assigned IPV4 addresses. 

4. Create Route Table
![route-table](C:\Users\marwa\Desktop\ceg3120\route-table.jpg)
![route-table-created](C:\Users\marwa\Desktop\ceg3120\route-table-created.jpg)
![route-table-subnet-association](C:\Users\marwa\Desktop\ceg3120\route-table-subnet-association.jpg)
![route-table-subnet-association-success](C:\Users\marwa\Desktop\ceg3120\route-table-subnet-association-success.jpg)
![routing-table-to-internet-gateway](C:\Users\marwa\Desktop\ceg3120\routing-table-to-internet-gateway.jpg)
![send-routing-table-rule-to-all-gateway](C:\Users\marwa\Desktop\ceg3120\send-routing-table-rule-to-all-gateway.jpg)
Route tables are set of rules which are also known as routes. These set of rules determine where network traffic is directed. Each route defines range of IP addresses where you want the traffic to traffic (the target/destination). Need a route for traffic within a subnet (other machines on your network). Need a route for traffic to the whole internet (other machines in the world). You can also associate a subnet with route table and if not then it is associated with main route table. 

5. Create Security Group
![security-group](C:\Users\marwa\Desktop\ceg3120\security-group.jpg)
![security-group-success](C:\Users\marwa\Desktop\ceg3120\security-group-success.jpg)
Securiy Group is a firewall at a network level. This works inside and outside of the VPC. Through this we can allow rules which are inbound and outbound. Acts as a virtual Firewall for EC2 instances to control inbound and outbound traffic

Part 2:
.
