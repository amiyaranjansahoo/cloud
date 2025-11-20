# jenkins jobs
```sh
Jenkins Types of Jobs 
In jenkins Job is a collection of steps(tasks) used for automation. There are different types of Jobs 
1. Freestyle Jobs (No coding) 
2. Pipeline Jobs (Modern & Important)
        a. Declarative Pipelines (V Important)
        b. Scripted Pipelines
```
## Jenkins Pipeline?
```sh
It is set of plugins to model jenkins jobs to deploy applications from source code to production using pipeline “as code”
A pipeline is a collection of steps or jobs which are interlinked with one another in a sequence.
Pipelines are also referred to as a “Deployment-as-a-Code”.
The Jenkins Pipeline is written into a text file called a Jenkinsfile (You can use a different name) which can be committed to a
 project’s source control repository.
A pipeline can be written using two types of syntax — declarative and scripted.
Both declarative and scripted pipelines are fundamentally the same pipeline sub-system underneath. They are durable
implementations of “Pipeline as code”. They both are able to use plugins and shared libraries. Where they differ however is in
syntax and flexibility.
```
## Types of Pipeline Jobs
```sh
2. Pipeline Jobs (Modern & Important) 
    a. Declarative Pipelines (V Important)
        Still Groovy under the hood, but with a structured syntax (predefined keywords like pipeline, stage, steps).
	    Easier to read and maintain.
    b. Scripted Pipelines
        Pure Groovy code.
	    You write everything manually using Groovy syntax.
```
## why jenkins pipelines
```sh
•	Code: Pipelines are implemented in code and typically checked into source control, giving teams the ability to edit, review,
    and iterate upon their delivery pipeline.
•	Durable: Pipelines can survive both planned and unplanned restarts of the Jenkins controller.
•	Pausable: Pipelines can optionally stop and wait for human input or approval before continuing the Pipeline run.
•	Versatile: Pipelines support complex real-world CD requirements, including the ability to fork/join, loop, and perform work
    in parallel.
•	Extensible: The Pipeline plugin supports custom extensions to its DSL footnote:dsl:[] and multiple options for integration with
    other plugins.

```
## Hello World Pipeline 
```sh
pipeline{ 
    agent any 
    stages{ 
        stage("Hello World"){ 
            steps{ 
                echo "Welcome to Jenkins Pipeline Job" 
            } 
        } 
    } 
}
```
## 
```sh
pipeline { 
    agent any 
    stages { 
        stage("Welcome") { 
            steps { 
                echo 'Welcome to Jenkins' 
                git branch: 'main', credentialsId: 'github-jan-25', url: 
'https://github.com/javahometech/lms-app/' 
                sh 'du -hs' 
                error "Testing" 
            } 
        } 
    } 
    post { 
      success { 
        echo "Send success email" 
      } 
      failure { 
        echo "Send failure email" 
      } 
    } 
}
```
