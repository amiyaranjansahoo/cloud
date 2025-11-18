## Jenkins installation types
```sh
There are various methods to install Jenkins.
Few of them are provided below
	Using yum
	Using war (using java)
	Using war (using tomcat )
  	docker
```
## Install Jenkins on Linux machine
```sh
Launch linux machine
Install java development kit.
	yum list all | grep jdk
	sudo yum install java-1.8.0-openjdk-devel –y
	sudo yum install 

# Download jenkins
Login to https://www.jenkins.io/ => Download => Under Download Jenkins 2.299 for: => Centos => Fedora => Redhat
Run the below commands 
  sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat/jenkins.repo
  sudo yum install jenkins

Start jenkins automatically when we reboot ec2.
  sudo chkconfig jenkins on

Start jenkins
  sudo service jenkins start

In this case the jenkins.war stored under /usr/share/java/jenkins.war /usr/lib/Jenkins/
```
## ec2 known limitation
```sh
Disk space is below threshold of 1.00 GiB. Only 471.49 MiB out of 474.78 MiB left on /tmp.
Dashboard => manage Jenkins => Nodes => Configure Monitor => Free temp space => Free space threshold = 20MB => Apply and save
```
