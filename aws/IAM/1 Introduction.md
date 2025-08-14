## IAM: Identity and Access Management
```sh
•	IAM is a service for managing permissions for users and services
•	We can share access to our accounts by add new users
•	We can manage service level permissions
•	We can handle programmatic access
    For example java code running on ec2 wants to upload files to S3, then we need to grant ec2 permissions
•	When we create AWS account, we use email Id (@gmail.com), debit card/credit card and password that is called as
Root user
•	Root account is having all permission to create/delete any resource
•	The organization creates root account but they never share that account to anyone
•	The organization can create one account to monitoring the EC2, but that account can’t do any other activities
•	Similarly the organization can create one account to manage EC2, obviously he can’t do any other activities
•	They will have login URL, and authentication. they can login and do their job
•	As a security best practise, we should not use Root user for day to day activities.
•	We have to create admin user and use it instead of Root
•	AWS strongly recommends that you do not use the root user for your day-2-day task, even the administrative ones
•	Use other IAM user accounts to manage the administrative task of your account 
•	Keep the root user credential in a secured and safe place and use them to perform only a few account and service
management task.
•	This is globally accessible i.e. if you create an user, it will be shown in AWS console irrespective of any regions
•	If we have one elb and that want to store S3 for storing the access logs, the IAM permission is required on
elb for S3.
```
<img width="940" height="444" alt="image" src="https://github.com/user-attachments/assets/5590cd89-c5f9-4f7d-8ecb-0716fa92ac07" />


## Cost
```
•	Its free to use
•	AWS IAM is a feature of your AWS account offers at no additional cost
```


