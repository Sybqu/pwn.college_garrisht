# Program and absolute paths
Invoke "challenge" correctly using absolute path
## My solve
**Flag:** `pwn.college{IqAyWTsPXtZA2ZoKQwWujolo8ZF.QX1QTN0wCOzAzNzEzW}`

```bash
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{IqAyWTsPXtZA2ZoKQwWujolo8ZF.QX1QTN0wCOzAzNzEzW}
hacker@paths~program-and-absolute-paths:~$ 

```
challenge is in / and run is in /
so the given absolute path helped me run "run" command

## What I learned
Continuation of absolute path.
"Run" is located inside "challenge" which in turn is located in root directory
hence the absolute path /challenge/run gave em the flag
## References 
.