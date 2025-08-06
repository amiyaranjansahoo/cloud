## Application Load Balancer
```sh
--> ALB can be used to balance the load across multiple targets if the request is HTTP or HTTPS or
gRPC [TCP Protocol], with SSL (Socket Layer security).
--> Operates at Layer 7 (Application Layer.)
--> AWS Launched ALB in the Year 2016 August 11.
--> This load balancer is best designed for load balancing of HTTP/ HTTPS traffic and 
    can route the incoming traffic towards the latest application architectures that include IP addresses, containers,
EC2 servers, and Lambda functions.
--> The application load balancer is optimized to work with traffic that is routed to targets within the Amazon
 Virtual Private Cloud (or Amazon VPC).
→ Examples: Web Applications, Website Hostings
```
## Task
```sh
 1. Create an Application Load Balancer to distribute the load across multiple websites running on 2 EC2 instances.

	a) Create 2 Linux EC2 instances with 2 different websites across different availability zones

	b) Create a target Group "ALB-TargetGroup" and add the above 2 servers as targets into the target group

	c) Create an Application load balancer and send the traffic to the Target group "ALB-TargetGroup"

	d) note down the DNS Name of the Application Load Balancer.

	DNS →  Application-Load-Balancer-2026724896.us-east-1.elb.amazonaws.com

2. Access the website using the application Load balancer DNS

NOTE: Traffic will be distributed across all the servers using Round-Robin Method by default.

Pricing → ALB & NLB are free-tier eligible upto 750 hrs per month.
```
