## Git Stashing(Stash Memory):
```sh
1. Stashing/stash memory in git will be used to keep the changes/modifications on the tracked files aside without
committing to the Local Repository temporarily & whenever we want that changes to be commit we can get back from
 the stash memory.
2. By default stashing will be apply on the Tracked files only & if required we can apply on the untracked files also
 by using some options.
```
## Move/keep the changes of the tracked file in stash memory
```sh
git stash
(or)
#git stash push
```
## List the changes in stash memory
```sh
git stash list
```
## get back the changes to the Project from stash memory
```sh
git stash apply
git stash apply stash@{<index value>} #This command will get back the changes which pushed lastly or latest change, that is LIFO
Ex:
git stash apply stash@{0} # This command will get back the changes by using specific index value of stash

Note:
"apply" command will get back the copy of the changes from stash memory in which original copy will still available in the stash
To delete the original copy from the stash we can use the following command
git stash drop

To get back the changes & delete the changes in the stash at a time we can use the following command
git stash pop
(or)
git stash pop stash@{0}
"pop" command is the combination of "apply" & "drop"
```




