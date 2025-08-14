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
•	It is a global service
•	It is a lifetime free service
•	IAM allows you to manage users and their level of access to the AWS console.
•	IAM is a web service that helps you securely control access to AWS resources.
•	IAM is used to control who is authenticated (sign-in process ) and who has authorization ( permissions) to access
all the AWS resources.
•	If we have one elb and that want to store S3 for storing the access logs, the IAM permission is required on
elb for S3.
```
<img width="940" height="444" alt="image" src="https://github.com/user-attachments/assets/5590cd89-c5f9-4f7d-8ecb-0716fa92ac07" />

## Differences Between Root User and IAM User
```sh
##### Root User:
•	Permissions: The root user has full access to all AWS services and resources. It cannot be restricted or limited in its
permissions.
•	Security: The root user has unrestricted access to the AWS account, making it a security risk if the credentials are
compromised.
•	Best Practice: AWS recommends that the root user not be used for everyday tasks and that its credentials be stored
securely.
•	Use Cases: The root user is typically used for initial setup and management of the AWS account, such as creating
IAM users and setting up billing preferences.

##### IAM User:
•	Permissions: IAM users have permissions that are assigned to them based on policies. These permissions can be limited
and restricted to specific services and actions.
•	Security: IAM users have limited access to the AWS account based on the permissions assigned to them, reducing the 
risk if their credentials are compromised.
•	Best Practice: IAM users should be used for everyday tasks and should be assigned the minimum permissions necessary
to perform their job functions.
•	Use Cases: IAM users are used for day-to-day operations in AWS, such as accessing resources, managing configurations,
and performing administrative tasks.
```
## Components Of IAM:
```sh
•	There are four Components of IAM:
    o Users
            IAM users are entities that you create in AWS to represent the people or services that interact with AWS services.
Each user has a unique set of security credentials.
   o User Groups
            Groups are collections of IAM users. You can assign permissions to groups, making it easier to manage permissions
for multiple users.
    o Roles
            IAM roles are similar to users, but they are intended for temporary use by applications, services, or other entities.
Roles have policies attached to them, which define the permissions that the role has.
    o Policies
            IAM policies are JSON documents that define the permissions for users, groups, and roles. Policies can be attached to
users, groups, and roles to grant or deny access to AWS resources.
```
