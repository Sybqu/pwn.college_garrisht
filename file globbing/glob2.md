# Matching with  ?
Starting from your home directory, change your directory to /challenge, but use the ? character instead of c and l in the argument to cd! Once you're there, run /challenge/run for the flag!

**Flag:**pwn.college{ckXT-CgArrg6lqYdJ6CR5C9mUmF.QXyIDO0wCOzAzNzEzW}




```bash
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
hacker@globbing~matching-with-:~$ cd ?a??enge
bash: cd: ?a??enge: No such file or directory
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
hacker@globbing~matching-with-:~$ cd ?ha??enge
bash: cd: ?ha??enge: No such file or directory
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
hacker@globbing~matching-with-:~$ cd ?ha??enge
bash: cd: ?ha??enge: No such file or directory
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{ckXT-CgArrg6lqYdJ6CR5C9mUmF.QXyIDO0wCOzAzNzEzW}
hacker@globbing~matching-with-:/challenge$ 






```
!
## What I learned
File Globbin using single wildcard character "?" basically repalces ? with any single characters ><
If zero files are unmatched the glob remains unchanged  
* the glob matches anypart except or leading "." character
## References 
.