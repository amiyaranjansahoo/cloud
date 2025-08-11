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
•	This is cost effective way of scaling
•	Autoscaling itself is free but we are charged for ec2 instances it launches.
```
## 
<img width="624" height="416" alt="image" src="https://github.com/user-attachments/assets/150a9bef-1920-48c5-87d7-906ca1593c40" />

## launch templates vs launch configurations
```sh
EC2 console only supports creating Auto Scaling groups with launch templates
Creating Auto Scaling groups with launch configurations is not recommended
```
## 1. Launch Template
```sh
•	Launch Template is a template used by auto scaling groups for launching ec2 instances.
•	The type of instance will be scaled out or scaled in, It will be defined by launch configuration
```
#### Launch Template need to define the following details
```sh
•	AMI to use
•	Private Key (Pem file)
•	EBS volume details
•	Security Group
•	IAM role
•	Instance Type
```
## 2. Auto scaling group 
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

## 3. Scaling policy => Metric type, target value
```sh
•	Defines how much you want to scale based on defined conditions
•	ASG uses alarms and policies to determine scaling.

Example:
Metric type:
CPU utilisation ( If CPU utilisation is more than 80 % , add one EC2)
and ( if CPU utilisation is less than 30 % decrease 1 EC2 )
```

## Health check 
```sh
Health check grace period:
Let say we have our AMI, one EC2 on top of that we have tomcat, on top of that we have java application
deployed. lets say it takes 60 seconds to come up fully including the EC2+tomcat + java deployment. If the health check was
performed before 60 sec, then the AS will terminate the EC2 and try to launch one more same set EC2+tomcat + java and its keep on
going in a infinite loop. Hence this parameter should be chosen more than 60 sec in current case example.

Default Cool down:
For example 300 sec, Once the AS adds EC2, up to next 300 sec, it won’t add any further EC2 though the conditioned matched to
add further EC2 )
The time duration gap between two scale in / scale out instances. 
Lets say at 09:15 one scale out happened ( 1 EC2 added), and once again there is a requirement at 09:17 to add one more EC2,
weather the EC2 will be added or not depending upon the configured value
```
