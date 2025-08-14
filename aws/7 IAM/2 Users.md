
# Users
```sh
•	An IAM User is an entity created in AWS that provides a way to interact with AWS resources.
•	The main purpose of IAM Users is that they can sign in to the AWS Management Console and make requests to the
 AWS services.
•	The newly created IAM users have no password and no access key. If a user wants to use the AWS resources using
 the AWS Management Console, you need to create the user password. If a user wants to interact using the AWS
programmatically (using the CLI (Command Line Interface)), you need to create the access key for that user.
The credentials created for IAM Users are what exactly uniquely identify themselves to AWS.
•	The security of the user's credentials can be enhanced by using the feature, i.e., Multi-Factor Authentication.
•	The newly created IAM Users do not have permissions, i.e., they are not authorized to access the AWS resources.
•	IAM users are not separate accounts; they are users within your account.
```
## IAM User Access Types
```sh
1. AWS Management Console Access
    Can login to AWS Account using Browser
    Will Get Username & Password
2. Programmatic Acccess
    Can Login to AWS Account using CLI, SDK or API
    Will get Access Key ID & Secret Access Key
```
