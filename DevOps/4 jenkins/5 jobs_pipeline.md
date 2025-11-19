# jenkins jobs
```sh
Jenkins Types of Jobs 
In jenkins Job is a collection of steps(tasks) used for automation. There are different types of Jobs 
1. Freestyle Jobs (No coding) 
2. Pipeline Jobs (Modern & Important) 
    a. Declarative Pipelines (V Important) 
    b. Scripted Pipelines
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
