
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


