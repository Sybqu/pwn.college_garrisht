# Redirecting errors
in this challenge, you will need to redirect the output of /challenge/run, like before, to myflag, and the "errors" (in our case, the instructions) to instructions.


**Flag:**pwn.college{IhghRal8iWXblHNn6f03DzfTc5R.QX3YTN0wCOzAzNzEzW}






```bash
hacker@piping~redirecting-errors:~$ /challenge/run >myflag 2>instructions
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{IhghRal8iWXblHNn6f03DzfTc5R.QX3YTN0wCOzAzNzEzW}

hacker@piping~redirecting-errors:~$ cat instructions
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will check that error output is redirected to a specific file path : instructions
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!

[TEST] You should have redirected my stderr to instructions. Checking...

[PASS] The file at the other end of my stderr looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-errors:~$ 
```
!
## What I learned
Standard output can be redirected to files
This can be done using > character.
File descriptor numbers are communication channels in linux
FD 0
FD 1 
FD 2
standing for standard: input,output and error respectively
hence all these can be redirected to other files
## References 
.