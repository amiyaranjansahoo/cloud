# Introduction
```sh
•	DNS: Domain Name System
•	This is used to convert the domain name to IP address. 
•	When we type www.google.com,the DNs server converts the domain name to IP 8.8.8.8
and connect to google.com.
•	This IP 8.8.8.8 is a public IP and this is unique in internet.
•	Like wise AWS has the Route 53 server which converts the DNS name to IP address.
•	You can use Amazon route 53 to register new domains, transfer existing domains
route traffic for your domains to your AWS external resources and monitor health
of your resources.
•	Let’s say I am going to create a new domain, www.cloud.com, first I have to buy
 the domain cloud.com, if its available I can buy and register. If its not available
 then I have to go for other domain names.
•	Like godaddy, AWS also provides domain name and you can buy the domain from AWS
 instead of going to godaddy
•	     DNS management
•	    Traffic management
•	    Availability Monitoring
•	    Domain  registration
•	AWS supports 2 types of domain.
•	    Generic level domain ( .com, .org, .net)
•    	Geographic level domain ( .in, .us etc)
```
<img width="940" height="460" alt="image" src="https://github.com/user-attachments/assets/071eb48c-8e60-41f0-9834-0bee2b1e92ec" />

## Route 53 Functions
```sh
•	Register a domain
•	As a DNS, it routes internet traffic to the resources for your domain.
•	Check the health of your resources
•	Also you can choose to receive notifications when choose to route internet
traffic away from unhealthy resources.
•	You can also use Route 53 for any combination of these functions:
•	For example: you can use Route 53 both to register your domain name and to
route  internet traffic for the domain.
•	Or you can use Route 53 to route internet traffic for a domain that you
registered with another domain register 
•	For example you have bought/register the domain from godaddy and later you
 migrated  to AWS ( in order words your server is in AWS) in that case you can
 also use the Route53 to redirect to AWS.
```
