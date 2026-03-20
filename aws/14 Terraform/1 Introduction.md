
## Infrastructure As Code(IAC):
```sh
1.	Provisioning infrastructure using the code
2.	Benefits:
    a.	Recreating infrastructure is easy and quick.
    b.	We put the code in SCM (Source Code management) tools like Git, SVN, etc. this gives the ability
        i.	review the changes before pushing to live
        ii.	SCM maintains all the versions of our code, we can quickly troubleshoot issues and even roll back if required.
3.	Tools for implementing IAC:
  a.	Terraform
      i.	Terraform is from HashiCorp and it has open source and enterprise versions.
      ii.	Terraform is more dynamic
      iii.	It uses HashiCorp Configuration Language ( HCL) 
      iv.	Syntaxes are easy and simple
      v.	It also allows you to define the code / templates more modular and reusable.
      vi.	It can support multiple cloud providers like AWS, Azure, GCP, Digital Ocean, Vmware etc.
  b.	AWS Cloud Formation
      i.	It’s from AWS and it works only for AWS.
      ii.	open source
      iii.	it uses JSON/YAML for writing your templates
  c.	Ansible
  d.	Chef
  e.	Puppet
  f.	Python
  g.	Java
```
<img width="766" height="371" alt="image" src="https://github.com/user-attachments/assets/850aa3ac-70de-4010-a19a-eedaee993f2b" />

### Download and configure terraform.
```sh
https://www.terraform.io/ => Download CLI => Windows 64 bit
1.	Download the binary => terraform_1.0.4_windows_amd64.zip ( Always go for the latest version)
2.	Unzip the package, folder contains one single binary file.
3.	Either set the path of the unzipped one or in the existing path (already set) copy the binary.
How to locate where terraform is installed:
C:\Users\608045267>where terraform.exe
```

### How to add terraform to path:
```sh
search system => Advanced System setting => Advanced => Environment variables . Now Go to lower window ( System variables =>
Click on new => and add the path
```
### Tools used to access terraform
```sh
1.	Git bash / Command prompt
2.	Choosing Editor for writing terraform code

•	We can use git bash or simple command prompt to access and run the terraform commands.
•	The AWS CLI must have been installed and path should be set.
```

### Configuring AWS access to Terraform:
```sh
Creating the user
•	Create an user say terraform in IAM aws console.
a.	Select Access type as Programmatic access
b.	Go to next screen and Attach existing policies directly (AdministratorAccess etc.. )
c.	Create the user
        Configuring the user
•	Configuring access key and secret key using AWS CLI
a.	As stated above the CLI must have installed already
b.	Setting up access key and secret key as environment variables.
•	Open the git bash and run the below commands
•	aws configure
```




