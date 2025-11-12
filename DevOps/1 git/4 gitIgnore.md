## Managing Files with .gitignore
```sh
we learned how to add files using the git add command. 
But here comes a new challenge: what if you don’t want some files to ever enter the staging area at all? 
That’s where the .gitignore file comes in.
```
Let’s create a few files first:
touch application.c module.pyc output.exe application.log output.out
git status # will show all files as untracked
Creating a .gitignore File
```sh
# Ignore compiled Python files
*.pyc

# Ignore log files
*.log

# Ignore executables
*.exe
*.out
```
Checking Status Again
```sh
git status
git add .
git status
```
