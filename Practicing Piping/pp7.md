# Grepping live outputs
/challenge/run will output a hundred thousand lines of text, 
including the flag. grep for the flag!
**Flag:**pwn.college{Uxgh928HRDhYC6naPj_79hw2Elf.QX5EDO0wCOzAzNzEzW}










```bash
hacker@piping~grepping-live-output:~$ /challenge/run | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stdout : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{Uxgh928HRDhYC6naPj_79hw2Elf.QX5EDO0wCOzAzNzEzW}
hacker@piping~grepping-live-output:~$ ^C
hacker@piping~grepping-live-output:~$ 

```
flags begin with pwn.college
used the pipe operator to remove the "middle men"
## What I learned
using PIPE | operator.
## References 
.