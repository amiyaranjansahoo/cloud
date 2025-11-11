## Verify the commits in the Local repository:
```sh
git log
This command will show the commits with "sha1" number or hexadecimal number with complete details.

git log --oneline
To see the commits in single line, use the following command:
```
## To see the content of the commits:
----------------------------------
```sh
git show <sha1 number>
Ex: git show 04735df

Note:
-----
Sha1 number is a random and unique 40 character hexadecimal value (0-9,a-f)
It will be created automatically by the git while commit the code/files
```
## Verify the difference between commits:
```sh
git diff <sha1 number>..<sha1 number>
Ex: git diff 56dc1ba..ac3f591
```
## Verify the commits during specific periods:
```sh
git log --since=<yyyy-MM-DD>
Ex: git log --since=2025-03-01

git log --until=<yyyy-MM-DD>
Ex: git log --untill=2025-03-10
```

## Verify the commits using author name:
```sh
git log --author="<name>"
Ex: git log --author="amiya"
```

## Verify the commits with multiple options in the single command:
```sh
git log --online --author="amiya" --since=2024-05-10
```


