## Jenkins
```sh
The leading open source automation server.
Jenkins provides hundreds of plugins to support building, deploying and automating any project.
Jenkins is used by the majority of devops teams.
it’s a CI/CD automation server that runs jobs via plugins and scripts
You can integrate SonarQube, Nexus, or Artifactory for code quality and artifact management.
Jenkins is written in java. # Hudson was the previous name
There are alternatives to Jenkins like
	GitHub Actions
	GitLab CI/CD
	CircleCI
	TeamCity
	AWS CodePipeline
	Azure DevOps
```
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

