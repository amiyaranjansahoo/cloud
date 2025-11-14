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
## Maven Repository
```sh
There are three different types of repositories

Central Repository (Hosted by maven in internet)
	By default dependences are downloaded from central
Local Repository
	The machine where we run maven commands
	Local repository avoids going to central reposioty everytime,first time dependency is downloaded from central and
    next time onwards use the copy present in local repository.
	Default local repository path (~/.m2/repository) 
Remote Repository
	Remote repository is used for couple of reasons
	To centrally store artifacts
	To store dependencies within organizations network
	Sonatye Nexus & JFrog Artifactory are commonly used for seting up Remote repository.
```
