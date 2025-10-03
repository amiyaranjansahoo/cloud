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
## 	Route53 hosted zone:
```sh
•	A route53 hosted zone is a collection of records for a specified domain.
•	The hosted zone where our name server and SOA of my domain reside/hosts.
•	You create a hosted zone for a domain and then you create records to tell the
domain name system how you want traffic to be routes for that domain. # this is
 when you have bought the domain from outside like godaddy
•	When we create/bought a DNS in route 53, automatically the hosted zone and name
 server gets created but if we have bought/created the DNS outside of AWS, then we
 have to create the hosted zone and name server explicitly.
•	Basically a hosted zone is a container that holds information about how you want
 to route the traffic for a domain and its sub-domains.
•	www.cloud.com is the domain , support@cloud.com, info@cloud.com are the
sub-domains.
•	Hosted domains are of 2 types.
•	You can create public (internet) hosted zone or private (Internal) hosted zones.
private domain only accessible inside VPC.
•	For each public hosted zone that you create Amazon Route 53 automatically
creates a name server(NS) record and start of Authority( SOA) record. Do not change
 these record ( NS & SOA )
•	Route53 automatically creates name sever ( NS) record with the same name as your
hosted zone, if you are creating the domain in AWS route53..
•	It lists the four name servers that are the authoritative name servers for your
 hosted zones.
•	Do not add, change or delete name server in this record.
•	When you create a hosted zone, AMAZON route53 automatically creates a name
Server (NS) records and a start of authority record (SOA) for the zone.
•	the NS record identifies the four name servers that you give to your register
 or your DNS service so that DNS queries are routed to Route53 name servers.
•	By default, Route53 assigns a unique set of four name servers ( known
collectively as a delegation set) to each hosted zone that you create.
•	  ns-1337 awsdns-39.com
•	  ns-895 awsdns-47.net
•	  ns-428 awsdns-s3.org
•	  ns-1597 awsdns-07.co.uk

```
## Route53 hosted zone default entries:
```sh
Inside the hosted zone by default you have 2 entries.
NS entry: Contains the unique sets of name servers for the hosted zone.
SOA entry: Contains information about the hosted zone.
```
## SOA
```sh
•	Start Of Authority
•	It’s another record like NS
•	stores important information about a domain or zone
•	The important information could be the email address of the administrator, when
 the domain was last updated, and how long the server should wait between refreshes
```



