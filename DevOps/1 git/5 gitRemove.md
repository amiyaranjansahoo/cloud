## Remove Files from Git Staging Area and Working Directory
#### Adding a Wrong File
```sh
echo "This is a bug file" > wrongfile.txt
git add wrongfile.txt
git status
```
#### Remove File Only from Staging Area (Unstage) but keep in working dir
```sh
git rm --cached wrongfile.txt

Result:
File goes back to untracked state.
File is still available locally in your directory.
```

#### Remove File from Staging + Working Directory
```sh
git rm -f wrongfile.txt

Result:
File is removed from staging area.
File is also deleted from your disk.
This is useful when you know the file is not needed at all.
```
#### Difference Between git rm and Linux rm
```sh
rm wrongfile.txt

Result:
File is deleted from your working directory.
But it still remains in Git’s staging area.
```
## Key Learning
```sh
Use git rm --cached → remove only from staging (keep file locally).
Use git rm -f → remove from both staging and working directory.
Using Linux rm alone will not unstage the file — it just deletes it locally.
```

