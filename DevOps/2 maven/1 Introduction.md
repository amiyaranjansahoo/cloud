## Maven
```sh
Maven is an automation and project management tool developed by Apache Software foundation.
It builds the project easily without any manual intervention
A build tool take care of everything for building a process.
It does the following.
	Generate/Fetch the source code from hub
	Compile the source code
	Install the package in local repo, or remote repo or central repo
Easy to add new dependency
It generates the reports
It maintains the release versions
It is based on POM ( Project Object Model)
Maven can build any number of projects 
Mostly used for java based project.
Maven is written in java.
Maven helps in getting the right jar file for each project as these may be different versions of separate packages.
When we build a project using anyt framework like struts, hibernate we need a lot of dependencies/jars/library.
To download dependencies, it is no more needed to visit the official website of each software.
It could now be easily done by visiting [mvnreopository.com](https://mvnrepository.com/)
Multiple jars: In order to build a project using  some technology like hibernate / spring we need a lot of jars.
And maven takes care of that without any headache.
It resolves the dependency of jars automatically. 
It downloads the correct version of jars.
```
## Build tool name
```sh
Java	- Ant, maven, gradle
C, C++ - Make file
Dotnet - MSBuild
Python - Setuptools, Poetry, PyBuilder
```
## Download and install maven
```sh
yum list all | grep -i java | grep corretto # java installation is mandatory 
sudo yum install java-11-amazon-corretto-devel.x86_64 # java installation is mandatory
git clone https://github.com/amiyaranjansahoo/docker-cicd-students-demo.git
wget https://dlcdn.apache.org/maven/maven-3/3.9.11/binaries/apache-maven-3.9.11-bin.tar.gz
tar -zxvf apache-maven-3.9.11-bin.tar.gz
mv apache-maven-3.9.11 maven-3
rm apache-maven-3.9.11-bin.tar.gz
cd maven-3/bin
./mvn
```

## Maven Repository
```sh
There are three different types of repositories

Central Repository (Hosted by maven in internet)
	By default dependences are downloaded from central
	It is available over the Internet, and anybody can access it.
	https://repo1.maven.org/maven2
	Dependencies are downloaded from the internet when you run maven build command.

Local Repository
	The machine where we run maven commands
	Local repository avoids going to central reposioty everytime,first time dependency is downloaded from central and
    next time onwards use the copy present in local repository.
	Default local repository path (~/.m2/repository) 
Remote Repository
	Certain customers do not use the central repository for security policy reasons.
	Then we need to setup remote repository within the customer network
	To setup remote repository, popular tools are
		Sonatype Nexus
		Jfrog Artifactory
	Remote repository is used for couple of reasons
		To centrally store artifacts
		To store dependencies within organizations network
```
## Maven Build lifecycle
```sh
The lifecycle of maven is as follows

Validate: 
	It validates pom.xml for the syntaxes and details that are required to perform build activity.

Compile:
	This phase compiles java code

Test
	Executes Junit test cases

Package
	Creates artifacts like (jar, war, war)

Verify
	This is used to take some actions based on test cases results to meet quality criteria.

Install
	Copies artifacts to local repository

Deploy
	Uploads artifacts to remote repository
	This requires configuration of remote server details.
```
## Maven target folder
```sh
Maven generates this folder to create artifact
mvn clean command deletes target folder
mvn clean package deletes target folder and create fresh target
```
