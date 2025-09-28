# Matching with *
using globbing to change directory at most 4 characters

**Flag:**pwn.college{sihc0Y41r24Q1AGyh091ul9QemH.QXxIDO0wCOzAzNzEzW}




```bash
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
hacker@globbing~matching-with-:~$ cd /*
bash: cd: too many arguments
hacker@globbing~matching-with-:~$ cd *
bash: cd: too many arguments
hacker@globbing~matching-with-:~$ cd /*ge
hacker@globbing~matching-with-:/challenge$ /challenge/ru 
bash: /challenge/ru: No such file or directory
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{sihc0Y41r24Q1AGyh091ul9QemH.QXxIDO0wCOzAzNzEzW}
hacker@globbing~matching-with-:/challenge$ ^C
hacker@globbing~matching-with-:/challenge$ 






```
!
## What I learned
File Globbin using wildcard character "*" basically repalces * with anything ><
If zero files are unmatched the glob remains unchanged  
* the glob matches anypart except or leading "." character
## References 
.