<img width="940" height="419" alt="image" src="https://github.com/user-attachments/assets/e312d2ef-40d0-4293-98a3-ac6d62699f92" />

## EventBridge? 
```sh
•	EventBridge is all about event‑driven architectures, and an event is a change in state. 
•	So imagine services like AWS Config, CloudTrail, and CloudWatch, all generating events relating to various changes
 in state in our AWS account.
•	And these events can be sent to EventBridge, and within EventBridge, we can configure rules which match the events
 and route them to the correct target. 
•	And targets define an action that will be taken on an associated AWS service. 
•	For example, shutting down an EC2 instance that has been marked as non‑compliant by AWS Config, or triggering a
Lambda function to take some action on your behalf in response to an event, or sending an SNS notification to notify
 you of an event in CloudTrail or CloudWatch. 
•	Now, EventBridge can also be used to schedule events. So we can create EventBridge rules which run on a schedule
that we define. 
•	For example, once an hour or once a day. Or using a cron expression, we can set a rule to run at the same time on
 a specified day, week, or month. 
•	Say, for example, you want to reboot a particular instance every month at the same time. You can do that using a
scheduled event in EventBridge
