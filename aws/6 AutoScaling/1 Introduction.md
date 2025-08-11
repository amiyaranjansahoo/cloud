## What is Auto Scaling
```sh
•	One of the important reason to migrate cloud is scalability, fault tolerance, high availability.
•	This can be done using the auto scaling.
•	To increase/decrease the resource as per requirement - which is called as scale, and automatically
happening is auto scaling
•	Auto scaling is one of the nicest features in cloud
•	It removes the pain of guessing and planning capacity
•	Auto Scaling automatically adjusts the capacity based on the load
•	Auto scaling adds new instances when needed and terminates instances when not needed.
•	Auto scaling is region specific.
•	We can’t configure the AS between two regions. Let’s say I have one server in India and one in
Singapore. We can’t configure the AS in this condition.
•	Let’s say I have 3 AZs. And in case Auto Scaling is enabled, then we should add the additional server
to all AZs evenly and equally. Once we select all AZs, it will add the additional server on its own by AWS
•	Creating group of EC2 instances that can scale up ( scale out) or scale down (scale in) depending on
conditions you set
•	Enable elasticity by scaling horizontally through adding or terminating EC2 instances
•	Auto Scaling supports horizontal scaling means increasing additional similar EC2 instance
(same CPU, RAM , N/W). 
•	Auto Scaling does not support vertical scaling means increasing the resources (CPU, RAM, N/W)) inside
the same EC2, which is obviously not a perfect solution.
•	Auto scaling ensures that you have the right no of AWS EC2 instances for your needs at all time.
•	This is very much cost effective.
•	You can select the spot or on-demand EC2 for auto scaling. 
•	You can integrate the ELB with AS and this is highly recommended.
```
## 
<img width="624" height="416" alt="image" src="https://github.com/user-attachments/assets/150a9bef-1920-48c5-87d7-906ca1593c40" />

## Launch Template
```sh
•	Launch Template is a template used by auto scaling groups for launching ec2 instances.
•	The type of instance will be scaled out or scaled in, It will be defined by launch configuration
```
## Launch configuration need to define the following details
```sh
•	AMI to use
•	Private Key (Pem file)
•	EBS volume details
•	Security Group
•	IAM role
•	Instance Type
•	You can’t edit launch configuration. You can create or copy
```
## Auto scaling group 
```sh
•	We need to define the Group name, , group size (minimum and maximum), VPC, Subnet, health check period
•	Its group of EC2 instances part of autoscaling
•	These instances are launched and terminated by autoscaling
•	ASG has minimum size and maximum size
•	Desired capacity, this is decided at runtime, for example current capacity is 10 instances and due to
load desired capacity is 15 then ASG launches 5 new instances.
•	We can also integrate spot instances with auto scaling
•	We can edit the ASG later as per the requirement
```
