## Code for AWS VPC
Google => search for terraform vpc
```sh
resource "aws_vpc" "myvpc" {
  cidr_block       = "10.0.0.0/16"
}
```
```sh
1.	resource is a keyword , it can’t be changed
2.	"aws_vpc" is resource type and for VPC type of resource this  has to be used
3.	myvpc => This a name given to the newly create VPC. it can be any arbitrary name
4.	All the inputs which we are passing here are called as arguments
5.	Once the VPC is created, then it will return couple of items called as attributes example vpcid etc etc
6.	In above arguments, only cidr_block is mandatory, rest all are optional 
7.	In case we wants to create one more VPC, that should not have same logical name myvpc
8.	But we can have another resource example subnet as logical name as myvpc
```

##### terraform init:
```sh
•	The terraform init command is used to initialize a working directory. 
•	This is the first command that should be run after writing a new Terraform configuration.
•	It is safe to run this command multiple times.
```
##### terraform apply
```sh
•	This command executes the action
```
##### terraform apply  -auto-approve
```sh
•	This command executes with auto approval
```
##### terraform plan
```sh
•	Dry run
```

##### terraform destroy
```sh
•	Destroy all the resource managed by terraform.
```
##### terraform destroy --target=
```sh
•	Destroy a particular resource managed by terraform.
```

+ => Creating the resource
-	=> Deleting the resource
~ => Updating/changing the resource

