## VPC

<img width="786" height="344" alt="image" src="https://github.com/user-attachments/assets/bfa124e4-b819-40fa-9888-3974fcb3fc97" />

```sh
•	VPC stands for virtual private cloud, its private cloud but virtual
•	VPC is a virtual  data centre inside AWS for one client. 
•	It is logically isolated from other virtual network in the AWS cloud.
•	No one can access/hack other VPC
•	Using VPC we can build virtually isolated data centres in the cloud.
•	With the help of VPC we can apply security to our resources.
•	VPC is must to deploy our compute resources in the cloud
•	VPC is free to use
•	Max 5 VPCs can be created and 200 subnets per VPC per region.
•	VPC is region specific, under which multiple availability zones are covered. 
•	Customers can create multiple VPCs within the same region or in different regions.
•	When we will created the AWS account, one VPC will be created automatically called as default VPC
•	This is customized VPC and we will create as per the requirement.
•	We can’t launch an EC2 instance just with VPC.
•	We need to have one or more subnetwork called as subnet in order to launch the EC2.
•	Once we created VPC DHCP(Dynamic Host Control protocol),NACL and security group,route table will get created
automatically.
•	Once the VPC is created, you can’t change its CIDR block
•	If you need a different CIDR size, create a new VPC
•	The different subnets within a VPC cant overlap
•	When you create a VPC, you must specify an IPv4 CIDR block for the VPC. 
•	The allowed block size is between a /16 netmask (65,536 IP addresses) and /28 netmask (16 IP addresses).
•	We can create multiple VPC of same CIDR in one account, one region.
•	Other user from other account also can create VPC of same CIDR in same region, where we have already created.
```
### Types of VPC 
```sh
There are 2 types of VPC
1.	Default VPC
2.	Custom VPC
```
### Subnet
```sh
•	Subnet is a smaller network inside VPC
•	Without subnet we can't launch ec2 instances
•	Subnet span availability zone
•	Two subnets CIDT can’t overlap.
```
### CIDR Calculation
```sh
CIDR to IP: https://www.davidc.net/sites/default/subnets/subnets.html
Visual Subnet Calculator: https://www.davidc.net/sites/default/subnets/subnets.html
```
### Types of Subnet 
```sh
There are 2 types of subnet
1.	Public Subnet
2.	Private Subnet
```
Subnet sizing for IPv4: https://docs.aws.amazon.com/vpc/latest/userguide/subnet-sizing.html
