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
sudo wget -O /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/redhat-stable/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
sudo yum upgrade
yum list all | grep -i java | grep corretto | grep 21 
sudo yum install java-21-amazon-corretto.x86_64 # java installation is mandatory
sudo yum install jenkins
sudo systemctl daemon-reload
sudo systemctl enable jenkins
sudo systemctl start jenkins
sudo systemctl status jenkins

In this case the jenkins.war stored under /usr/share/java/jenkins.war /usr/lib/Jenkins/
```
## How to access jenkins
```sh
http://ec2 public ip:8080
```
## ec2 known limitation
```sh
Disk space is below threshold of 1.00 GiB. Only 471.49 MiB out of 474.78 MiB left on /tmp.
Dashboard => manage Jenkins => Nodes => Configure Monitor => Free temp space => Free space threshold = 20MB => Apply and save
```
