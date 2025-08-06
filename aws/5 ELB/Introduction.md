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

