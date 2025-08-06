## Legacy IT system: ( Without ELB )
<img width="939" height="153" alt="image" src="https://github.com/user-attachments/assets/ff1833de-bc8b-4baf-a3c4-0343d04a8616" />

## Strategic IT system ( With ELB )
<img width="940" height="498" alt="image" src="https://github.com/user-attachments/assets/807ed99f-a0ab-4093-8a45-f698bdb82bd8" />

```sh
•	Load balancer distributes the web traffic to the available backend servers
•	Load balancer serves as a single point of contact on behalf of the backend server for your clients.
•	From user till LB is called as front end and from LB till DB called as backend
•	AWS offers ELB as PaaS
•	It is full managed by AWS
•	It is by default HA-High Availability, fault tolerance  and scalable
•	ELB is VPC specific, it can load balances EC2 instances in side one VPC
•	Load balancers perform health checks and route traffic to healthy instances.
•	If load balancer finds unhealthy instances it keep it out of service without terminating
•	ELB supports SSL (Security Socket Layer) termination.
•	SSL termination is the process of closing the SSL connection and decrypting the data
•	The SSL termination can be done at ELB or EC2 instance level
•	But SSL termination is expensive in terms of infra i.e. it consumes more CPU and memory and also ELB is auto scalable,
so ELB can manage the infra at SSL termination 
•	Its recommended to do SSL termination at ELB level not in EC2 level or in other way ELB is configured for SSL termination
```
## Health check parameters
```sh
Response timeout
  Default Range is 2-120 sec)# 5 seconds
	The ELB pings to EC2 for health check and the response should come to ELB within 5 sec( default value), if not then ELB
  will consider as unsucessful


Health check Interval 
The time interval between two ping request from ELB to EC2 is called as health check interval
	Period of time between health checks
	Defaults 30 seconds ( range is 5 to 300 sec)

Un-healthy threshold 
	The no of failure ping which will decide whether the EC2 is un healthy. 
	Let’s say the configured value is 2, after 2 consecutive ping which are un-success, then the EC2 will be declared as
  un healthy
	No of consecutive failed health check that should occur before the instance is declared un-healthy
	Default 2 ( Range 2 – 10)

Healthy Threshold
	No of consecutive successful health checks that must occur before the instance considered as healthy
	Default 10 ( Range 2 - 10)
```
## Types of Load Balancer
```sh
1. Classic Load balancer (this is the first one introduced by AWS)
	AWS says the previous generation load balancer donot use it.
	layer 4 and layer 7
	HTTP, HTTPS, TCP, SSL
2. Application Load Balancer(this is the second done introduced by AWS)
	7th layer – Application later of OSI
	HTTP/HTTPS ( port 80, 443)
3. Network Load balancer
	Very fast LB, big latency LB, need response in fraction of sec
	4th Layer – Transport layer
	Works on TCP, UDP, TLS protocol
4. Gateway Load balancer
```

