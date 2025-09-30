# Grepping live outputs
/challenge/run will output a hundred thousand lines of text, 
including the flag. grep for the flag!
**Flag:**pwn.college{UL1aiNfhnq32U8Hw4aiC2Gm10s3.QX1ATO0wCOzAzNzEzW}










```bash
hacker@piping~grepping-errors:~$ /challenge/run 2>&1 | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{UL1aiNfhnq32U8Hw4aiC2Gm10s3.QX1ATO0wCOzAzNzEzW}
hacker@piping~grepping-errors:~$ ^C
hacker@piping~grepping-errors:~$ 


```
flags begin with pwn.college
used the pipe operator to remove the "middle men"
i had a bit of problem as i kept grepping for pwncollege . T^T .(Wasted a lot of time).
## What I learned
using PIPE | operator. Directing standard errors and grepping through thems
## References 
.