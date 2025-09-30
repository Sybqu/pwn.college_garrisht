# Redirecting  more output
In this level, /challenge/run will once more give you a flag, but only if you redirect its output to the file myflag. Your flag will, of course, end up in the myflag file!


**Flag:**pwn.college{8uKlYkCXFfCAmkA3rF345OdcqAO.QX1YTN0wCOzAzNzEzW}






```bash
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ /challenge/run
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[FAIL] You did not satisfy all the execution requirements.
[FAIL] Specifically, you must fix the following issue:
[FAIL]   You have not redirected anything for this process' stdout.
hacker@piping~redirecting-more-output:~$ /myflag
bash: /myflag: No such file or directory
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{8uKlYkCXFfCAmkA3rF345OdcqAO.QX1YTN0wCOzAzNzEzW}

hacker@piping~redirecting-more-output:~$ 

```
redirected output and read from the new output file
## What I learned
Standard output can be redirected to files
Applicable to all commands (according to my current knowledge idk about exceptions)
This can be done using > character.
## References 
.