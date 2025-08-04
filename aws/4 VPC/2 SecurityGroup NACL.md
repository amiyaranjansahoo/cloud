## Security Group
```sh
•	Is a virtual firewall works at ENI ( Elastic Network interface) level.
•	It’s used to secure resources like ec2, rds, elb, lambda etc..
•	Security group has a bunch of rules to control traffic.
•	Security group has inbound and outbound rules.
•	Can only have permit rules, cant have any deny rules
•	Inbound rules are for securing inbound connections # Inbound means traffic for Inbound traffic
•	Outbound rules are for securing outbound connections # Outbound means traffic for Outbound traffic
•	Security groups are stateful, for inbound traffic it applies only inbound rules, when traffic gets
 out of ec2 it does not apply outbound rules.
•	There is no explicit allow/deny, a rule in security group allows implicitly
•	There is no way to block specific ip in security group
•	One security group can be linked to multiple EC2 instances
•	Each ec2 can have maximum 5 security groups # Select ec2 => action => security => change security group
•	Technically security groups are attached to elastic network interfaces.
•	We can attach same security group to multiple ec2 instances
•	Up to 5 security groups per EC2 instance interface can be applied
```
## NACL
```sh
•	NACL is one more layer of security
•	NACL acts at subnet level
•	NACL has inbound rules and outbound rules
•	NACL is stateless, it applies both inbound/outbound rules for all types of traffic.
•	NACL supports allow/deny, you can whitelist or blacklist ips.
•	NACL can be associated with multiple subnets
•	Your VPC automatically comes with a modifiable default NACL, by default it allows all traffic
 inbound and outbound
•	You can create custom NACL,  by default denies all inbound and outbound traffic.
•	Each subnet in your VPC must be associated with a Network ACL, if you do not explicitly associate
the subnet with a NACL, the subnet is associated with the default NACL.
•	You can associate a Network ACL with multiple subnet, however one subnet can be associated with only
one NACL at a time.
•	When you associate a NACL with a subnet, the previous association is removed.
•	NACL have rules with rule numbers
•	Rules are evaluated from lowest to highest
•	The highest rule number that you can use for a rule is 32766.
•	Its recommended to keep the rule numbers in a multiple of 100, so that you can insert the rules later
if needed
•	It functions at  subnet level
```
