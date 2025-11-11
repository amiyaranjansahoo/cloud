## Branches in Git:
## What is a Branch?
```sh
==>Branch is a series or collection of commits of files/code, that means development of code in the project will
 happens with in a branch only.
==>Branch is like a folder in the project
==>we can create "n" number or multiple branches in the project
==>By default there is a branch in the project known as "master/main"
==>Defaultly the development of code/files will be done in the "master/main" branch only
==>Branches in the project will be used for different reasons as follows:

->To develop the features of the project separately can be done in different branches for easy identification
 of features & finally we can merge all the branches in to a single branch to combine all the features/entire code
 of the project.
    
->To Separate the code of the Project in to different environments like Dev, Testing, UAT, Production we can
use branches, that means while deploying the code to the particular environment like Dev, Testing, UAT, Prod
 we can fetch the code from that particular branch.
```
## List the branches branches in the Project
```sh
git branch

Note: By default will be shown with default branch "master" & the current branch will be   represent with *
```

## create a new branch
```sh
git branch <branch name>
Ex: git branch feature
```
## To switch/move from one branch to another branch
```sh
git checkout <branch name>
Ex: git checkout feature
```
## To create & switch to the branch in a single step
```sh
git checkout -b <branch name>
Ex: git checkout -b LoginModule 

Notes:
=>While creating the new branches from the master branch or any other branch, then all the commits/code/files of the master branch will comes to new branches.
=>The new commits/files/code of new branch will not be available in the master branch untill/unless we merge/combine the new branch to master branch 
=>After creating the new branches from the master branch,then if you create new commit in the master branch then we cannot see that commit in the new branches,that is whatever the commits we had in the master branch at the time of creation of branches only those will comes to new branches
=>So,to see the new commits of all new branches in the master branch,we can merge/combine/mix all the new branches to the master branch.
```
