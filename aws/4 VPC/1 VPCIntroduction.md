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
### Components of VPC:
```sh
•	Route table
•	Internet Gateway
•	Security group
•	Network ACL
•	Peering connections
•	Elastic IPs
```

## Route table 
```sh
•	Routers are used for connecting different networks
•	A route table contains a set of rules, called routes, that are used to determine where network traffic from your subnet
is directed.
•	Route tables are used for
o	Connecting subnets within vpc
o	Connecting subnets to internet
o	Connecting a VPC with another VPC (vpc peering)
o	VPC to the Internet Gateway
o	etc
•	When vpc is created implicitly a route table is created that is called “Main” route table.
•	By default all subnets are implicitly associated with the “Main” route table.
•	We can have custom route tables, and we can explicitly associate subnets to the custom route table.
•	One subnet can be associated to one route table.
•	You can associate multiple subnets with the same one route table. 
•	It’s called as logical or implied router. 
•	It’s the central routing function
•	You can have 200 Route tables per VPC
•	You can have 50 Route entries per route table
•	Each subnet must be associated with only one route table at any given instance of time.
•	If you do not specify a subnet to route table association, the subnet will be associated with the default VPC Route table.
•	You can also edit the Main Route table if you need. but you can’t delete the main route table
•	However you can make a custom route table manually become the main route table ten you can delete the former main as it’s
no longer a main route table
•	Every route table has a default route, which allows a subnet to communicate with any subnet in the same vpc, we cannot
delete the default route.
```
## Attributes in Route table
```sh
•	Destination—The range of IP addresses where you want traffic to go (destination CIDR). For example, an external
corporate network with a 172.16.0.0/12 CIDR.
•	Target—The gateway, network interface, or connection through which to send the destination traffic; for example,
 an internet gateway.
•	Propagation—Route propagation allows a virtual private gateway to automatically propagate routes to the route tables.
This means that you don't need to manually enter VPN routes to your route tables. For more information about VPN
routing options, see Site-to-Site VPN routing options in the Site-to-Site VPN User Guide.
```
## Internet Gateway
```sh
•	An Internet Gateway is  a virtual router that connects a VPC to the internet
•	Default VPC is already attached with an Internet Gateway
•	If you create a new VPC then you must attach the Internet Gateway in order to access the internet.
•	Ensure that the subnet’s Route table points to the Internet Gateway
•	It performs the NAT between your private and public IPV4 address
•	It supports both IPV4 and IPV6.
•	Internet gateway provides internet access, both inbound and outbound
•	One internet gateway – I can use the same IG to multiple route table inside the same VPC 
•	We can attach the IG to one VPC at a time. We cant attach one IG to multiple VPC at a time.
```

