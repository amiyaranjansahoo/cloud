## What is AMI (Amazon Machine Image)
```sh
It's a template that contains the operating system and certain pre-installed tools.
```sh
#### Custom AMIs
```sh
In the real world most of the time custom AMIs are used.
Demo - Create Custom AMI
1.	Launch EC2 instance using existing AMI
2.	Install and configure the tools you need on this server
3.	Create Image —> custom AMI
4.	After creating an Image you can terminate the instance used in the first step.
You can Launch Instance Using Custom AMI.
```
#### AMI Permissions
```sh
1.	AMI is by default private
2.	We can share with other AWS accounts if required.
3.	AMIs can be made public (accessible to all AWS accounts)
4.	AMI is region specific.
```
#### Backup up EC2
```sh
Creating AMI is nothing but taking EC2 backup.
```

#### Exercises:
```sh
1.	Launch Instance with Ubuntu AMI in Mumbai Region
2.	Host a Static Website Using EC2 Instance.
(Use Nginx Web Server )
3.	Create Image for your Instance.
4.	Terminate Your Instance Manually.
5.	Re-Create Your Instance in N.virginia Region. 
```
