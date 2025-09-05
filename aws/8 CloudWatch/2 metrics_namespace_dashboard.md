## CloudWatch Metrics? 
```sh
•	A metric is simply a variable that you would like to monitor using CloudWatch. 
•	And CloudWatch metrics consist of a time‑ordered sequence of values or data points which are published
to CloudWatch. 
•	Each data point in a metric has a timestamp and optionally a unit of measurement. 
•	For example, think about the CPU usage on an EC2 instance and the unit of measurement will be a percentage. 
•	And CloudWatch metrics are uniquely defined by a name, a namespace, and zero or more dimensions.
```
## CloudWatch alarm
```sh
A metric alarm has the following possible states:
•	OK – The metric or expression is within the defined threshold.
•	ALARM – The metric or expression is outside of the defined threshold.
•	INSUFFICIENT_DATA – The alarm has just started, the metric is not available, or not enough data is available
 for the metric to determine the alarm state. The data is not sufficient to take any action
```
## CloudWatch Namespace
```sh
•	A namespace is simply a container for CloudWatch metrics. 
•	For example, EC2 uses the AWS/EC2 namespace, and you can create your own namespaces to publish custom metric
data. 
•	So when you want to publish custom metric data, you must specify the namespace for each data point or value
 that you want to publish to CloudWatch. 
•	And you specify the name of the namespace when you create the metric, and metrics from different namespaces
 are completely isolated from each other, so they are not aggregated. 
•	So metrics from different applications are not aggregated into the same set of statistics. So this means
 that you  can keep all the metrics that relate to a specific application in its own namespace. 
•	And in the CloudWatch console, your custom metrics will appear under custom namespaces. And here is where
you'll find all the custom metrics that are provided by the CloudWatch Agent, and they're grouped in their
own namespace, while the AWS metrics appear under the AWS namespaces section.
```
#### When to create custom namespace?
```sh
Imagine you’re running an e-commerce app on EC2:
•	AWS gives you default metrics (CPU, disk, network).
•	But you also care about business metrics, e.g.:
      Number of orders processed per minute
      Number of failed checkout attempts
      Average order value
```
#### How to create custom namespace
```sh
•	Launch ec2
•	Create a role for EC2 to send log file to cloudwatch.
	    Trusted entity type: AWS
	    Service or use case: ec2
	    Permission: CloudWatchAgentServerPolicy
# Install
sudo yum install amazon-cloudwatch-agent -y

# Configure
/opt/aws/amazon-cloudwatch-agent/bin/config.json

{
  "agent": {
    "metrics_collection_interval": 60,
    "logfile": "/opt/aws/amazon-cloudwatch-agent/logs/amazon-cloudwatch-agent.log"
  },
  "metrics": {
    "namespace": "MyApp/CustomEC2Metrics",
    "metrics_collected": {
      "mem": {
        "measurement": [
          "mem_used_percent"
        ],
        "metrics_collection_interval": 60
      },
      "disk": {
        "measurement": [
          "used_percent"
        ],
        "metrics_collection_interval": 60,
        "resources": [
          "/"
        ]
      }
    }
  }
}


# Start agent
sudo /opt/aws/amazon-cloudwatch-agent/bin/amazon-cloudwatch-agent-ctl \
  -a fetch-config \
  -m ec2 \
  -c file:/opt/aws/amazon-cloudwatch-agent/bin/config.json \
  -s

# Verify
```
## CloudWatch dashboard
```sh
•	CloudWatch dashboard is a custom view, just like a homepage that we create in CloudWatch. 
•	And we can use it as a single page for monitoring our resources. 
•	And we can create a CloudWatch dashboard to display important metrics for all of your production systems in
one place. 
•	For example, we might want to monitor the CPU and memory usage, and you can create a CloudWatch dashboard to
display important metrics for all of our production systems in one place. And this allows you to check the health
 of your critical systems and applications from one single dashboard.
```



