EC2 Instance Purchase Options (Important for cost optimization): https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-purchasing-options.html
#### On-Demand Instances
```sh
These instances are flexible to use, that is you get it when you want it and terminate it when you don't want it.
When compared with other purchase options this is costlier
Use on-demand when you don't need it for the long term.
1.	To work with POCs (Proof Of Concept)
2.	For example, Flipkart wants 20 additional servers only for a big billion day.


Billing:
-	When instance is in running state billing is on otherwise billing is off

Fixed price (Hourly )

Pay per what you have used.
- Pay per Hour
- No commitment 
- No Upfront Payment 
- No Predictable Usage.
```
#### Reserved Instance
```sh
We should give either one or three years commit in return we get significant discounts
Use this only when you need it for a minimum 1 year.
●	After buying reserved instance AWS will not take it back
●	You can sell it in marketplace
Billing
-	Your bill is fixed
-	Long term commitment 
-	1 or 3 years
-	Upfront payment (fixed , partial)
-	75% discount on hourly price
-	Standard RI - 75% discount 
-	Convertible Ri - to change capacity of the Instance anytime 
-	Scheduled RI - reserve it for short term like fraction of day or week.
```
#### Dedicated Hosts
```
-	We should use dedicated hosts when we want to bring your own license to cloud
-	AWS allocates the entire physical host to you.
```
#### Spot Instances
```sh
Amazon allocates EC2 instances from its spare capacity, you get up to 90% discounts.
→ The problem with spot instances is if someone pays more than you amazon can take this instance from you
and give it to other customers.
→ You buy spot instances by bidding, spot price depends on the demand and it keeps changing.
-	Bidding
-	Auctioning
-	Huge capacity for cheaper price
-	90% Discount.
Spot Interruption
Amazon can take the instance from you at any point of time by giving 2 minutes notice.
```
