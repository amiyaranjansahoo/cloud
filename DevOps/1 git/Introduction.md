
## GIT
```sh
Git is a Version Control System (or) Source Code Management System
Git is used to track the files/Code
It will maintain the multiple versions of the same file
It will allow collaboration between the developers while developing the code
It will keeps the records of the changes on the code by the developers
It will allows to know who made the changes & when
It will allows you to revert any changes
In Git developers will store the code in a location known as Repo/Repository, that is     nothing but a folder to store the code.
It is a Platform-Independent Tool
It is free & open-source
It will handle larger projects efficiently
It is written on "C" programming Language
It came in to the market on the year 2005
A version Control System will manage the changes to documents, computer programs,large websites & other collection of information.
```

## Installation of Git Tool:
#### In windows Machine:
```sh
 goto ---------->google
                   |
              search for "git" download
                   |
              select the first link for Git official website
                   |
              Then select the "downloads" for windows
                   |
              Then click download
                   |
       After downloading the git, click the setup file to install
                   |
 After installing the git in windows, will get with a git command prompt known as "git bash"
                   |
To check the version of git, open command prompt & use the command "git -v"
```
#### In Linux Machine:
```sh
-->here we can use a package manager command to install the git as follows:

                    #sudo yum install git

                            (or)

                    #sudo apt install git

--->After installation of git, to check the version we can use command as follows:

                    #git -v 
```
#### Initialisation of "git" in the Project Folder:

##### step1:
```sh
-->create the project folder like "Project1" in any location like "c" Drive in the local    windows machine
-->create simple html page like "index.html" in the project folder
```
##### step2:
```sh
-->Initialisation of "git" in the project folder
-->To initialise the git in the project folder we can use the following command

                              git init

-->To use the above command we can open a Command Prompt like "cmd" or "git bash"
-->Then change to the Project location in which your project folder contains as follows

                      c:\users\Maxhub>cd ..
                      c:\users>cd ..
                      c:\cd Project1
                      c:\Project1> git init

-->By using "git init" in the project folder will create three stages as follows:

                     1)Local Repository

                     2)Staging/Caching

                     3)Working Directory

-->By default by creating the code/file in project will be present in "Working Directory" which means in "untracked mode"

-->To track the files/code by the git, we should move the code/files from Working Directory to the "Staging/Caching"

-->In staging/caching, the code will be going to track by the git & store the records/history of the file/code changes

-->After that, move the code/files from staging/caching to the "Local Repository" for tracking

-->In "Local Repository" code/files are in tracked mode

-->Tracking means identifying the changes happening on the files/code & who are doing changes & when, like every thing will be stored as a history by the git tool
```
##### user level configuration:
```sh
-->First to work with git we should define user level details in the Project to be identify by the Git to know who are working on the Project.
-->To define user details we can use the following commands:

syntaxes:
---------
--->To define user name

      #git config --global user.name "<Name of user>"

   Ex:
   ---
         #git config --global user.name "satish"

--->To define user email

      #git config --global user.email "<Email address>"

   Ex:
  -----
          #git config --global user.email "<satish@gmail.com>"

--->To see the defined configuration

           #git config --list

--------------------------------------------------------------------------------------
Checking the status of code/files in the project:
--------------------------------------------------
-->To check the code/files whether that are in tracked or untracked mode
   we can use the following command

                         #git status

-->Initially this command will show the files in untracked mode in Red color, which means the code/Files are in Working directory. 

-----------------------------------------------------------------
Moving the code/files from Working directory to staging/caching:
---------------------------------------------------------------
syntax:
-------

             #git add <filename>

                    (or)

             #git add .

        Ex:
       ----
                #git add index.html

Note: --->Here . represents the all the files in the project
-----
-->After executing the above command will show the files in green color, which means in the staging/caching area.
-->To check the status again we can use the command as follows:

                  #git status

---------------------------------------------------------------------------------
Moving the code/files from staging/caching to the Local Repository:
-------------------------------------------------------------------
syntax:
-------

                   #git commit -m "<commit message>"

             Ex:
             ---
                    #git commit -m "<adding the files>"

--->The above command will move the data from staging/caching to the Local repository stage for tracking
--->After executing the above command, again we can check the status using the following command:

                      #git status

=============================================================================================
```
