# Multiple globs
We put a few happy, but diversely-named files in /challenge/files. Go cd there and run /challenge/run, providing a single argument: a short (3 characters or less) globbed word with two * globs in it that covers every word that contains the letter p.


**Flag:**pwn.college{YVTOds5QHyq4mP1wBElnMhP7iS0.0lM3kjNxwCOzAzNzEzW}






```bash
hacker@globbing~multiple-globs:~$ cd /challenge/files
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{YVTOds5QHyq4mP1wBElnMhP7iS0.0lM3kjNxwCOzAzNzEzW}
hacker@globbing~multiple-globs:/challenge/files$ 

```
easy ahh
## What I learned
Multiple globbing ><
Bash supports the expansion of multiple globs in a single word

## References 
.