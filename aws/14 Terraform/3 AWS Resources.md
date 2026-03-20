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

#### .terraform.lock.hcl
```sh
•	Post execution of terraform init this file gets created
•	This is a terraform Lock File
•	Terraform automatically creates or updates the dependency lock file each time you run the terraform init command.
•	This presents in  the current working directory
•	Terraform automatically creates or updates the dependency lock file each time you run the terraform init command.
•	You should include this file in your version control repository so that you can discuss potential changes to your
  external dependencies via code review,
•	It is named with the suffix .hcl instead of .tf in order to signify that difference.
```
#### .terraform
```sh
•	Post execution of terraform init this file gets created
•	This presents in  the current working directory
•	The .terraform directory is a local cache folder
•	Terraform uses this folder when acts on the configuration files. 
•	Its contents are not intended to be included in version control.
```
#### Terraform State File
```sh
terraform.tfstate
•	State file contains resource details created by terraform.
•	Terraform creates default state files automatically with the name terraform.tfstate.
•	This file is created when you run “terraform apply” for the first time.
•	This is called as terraform state file.
•	This state is stored by default in a local file named "terraform.tfstate", but it can also be stored remotely, which works
  better in a team environment.
•	It’s a json file automatically created by terraform.
•	Information about all resources created by terraform is stored in this state file.
•	When you run terraform apply, terraform compares state file with all your terraform files accordingly, it may add, update
  or delete
•	Never ever update this file on your own.
•	Terraform is idempotent ( if we apply same commands multiple times , it won’t create any side impact)
```
##### Code for subnet



