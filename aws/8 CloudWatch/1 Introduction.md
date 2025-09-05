## Amazon CloudWatch
```sh
•	Amazon CloudWatch is a monitoring service that allows you to monitor the health and performance of your
AWS resources, as well as the applications that you run on AWS and in your own datacenter
•	It can monitor EC2 instances, auto scaling groups, Elastic Load Balancers, Route 53 health checks, and Lambda
•	In terms of storage and content delivery, it also monitors the EBS volumes, storage gateway, and CloudFront. 
•	And for databases and analytics, it can monitor DynamoDB tables, ElastiCache nodes, RDS instances, Redshift,
and Elastic Map Reduce etc etc
•	And in addition to all of that, it can also monitor SNS topics, SQS queues, API Gateway, and it can even monitor
 your estimated AWS monthly charges.
•	There's also a CloudWatch Agent, which you can use to define your own custom metrics. 
•	And there's also CloudWatch Logs, which allows you to monitor operating system logs and application logs, and this
 allows you to create your own custom application monitoring solution
•	So let's take a look at how it works with EC2, for example. And by default, all EC2 instances send key health and
 performance metrics into CloudWatch.
•	And the default EC2 host‑level metrics consist of CPU, network, disk, and status check. 
•	And by default, CloudWatch metrics are stored indefinitely, and you can even retrieve data from any EC2 instance
 or Elastic Load Balancer instance, even after the instance has been terminated. 
•	By default EC2 does not send operating system‑level metrics into CloudWatch. 
•	However, by installing the CloudWatch Agent on your EC2 instances, you can collect operating system metrics and
send  them into CloudWatch.
•	And when I say operating system‑level metrics, the kind of thing I'm talking about is memory usage on your
instance, processes running on your instance, the amount of free disk space available on your instance, add CPU idle
 time, and  these are all operating system‑level metrics which you can only see inside the operating system
of your instance.
•	And the CloudWatch agent running on your instance can collect these metrics and send them into CloudWatch.
•	How much granularity you get with CloudWatch? How frequently are the metrics being sent? 

```
