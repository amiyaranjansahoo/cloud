To check the commits in the Local repository:
---------------------------------------------

                                  #git log

-->This command will show the commits with "sha1" number or hexadecimal number with complete details.
-->To see the commits in single line, use the following command:

                                 #git log --oneline


To see the content of the commits:
----------------------------------
syntax:
-------

                       #git show <sha1 number>

               Ex:
               ---
                         #git show 04735df

Note:
-----
-->Sha1 number is a random and unique 40 character hexadecimal value (0-9,a-f)
-->It will be created automatically by the git while commit the code/files

--------------------------------------------------------------------------------------------
To check the difference between commits:
----------------------------------------
syntax:
-------
           #git diff <sha1 number>..<sha1 number>

     Ex:
     ---
              #git diff 56dc1ba..ac3f591


To check the commits in periods:
--------------------------------
syntaxes:
---------

       #git log --since=<yyyy-MM-DD>

Ex:
---
        #git log --since=2025-03-01

                     &

       #git log --until=<yyyy-MM-DD>

Ex:
---
        #git log --untill=2025-03-10


To check the commits using author name:
---------------------------------------

syntax:
-------

               #git log --author="<name>"

           Ex:
           ---
                  #git log --author="amiya"


To check the commits with different options in the single command:
------------------------------------------------------------------

         #git log --online --author="amiya" --since=2024-05-10


