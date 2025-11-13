
<img width="1134" height="537" alt="image" src="https://github.com/user-attachments/assets/766dd876-0b44-4cfc-ad12-0b15c60c51a3" />

## Pull Vs Featch_Merge
```sh
"fetch" & "pull" is the process of getting/downloading the code/files from git server repository/project to local
 machine repository/project
"fetch" will get the code from git server remote repo to the local machine & will store in the remote repo copy
& then merge those files/code to the local repo manually.
"pull" will get the code from git server remote repo to the local machine & will store in the remote repo copy
 & will merge those files/code to the local repo automatically.
By using "fetch" we cannot see the new code/files of git server in the local repo untill we can merge those
files to the local repo.
By using "pull" we can see the new code/files of git server in the local repo directly.
By cloning or establishing the connection between the Git server & Local Machine then the Git Server Remote
Repo/Project copy will comes to the local machine along with branches
The remote repo branches in the local machine are known as "Remote Branches"
```
## To check the remote branches in the local machine then use the following command
```sh
git branch -a
By using the above command code/files will get to the local machine & will be stored in Remote Repo copy

 In order to see that new code/files in the local repo we should merge remote repo branch in to the local repo branch
 by using the following command:

git merge <remote_branch_name>

Ex:
git merge origin/master
```
