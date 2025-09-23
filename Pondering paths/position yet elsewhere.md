# Position yet elsewhere
his challenge will require you to execute the /challenge/run program from a specific path (which it will tell you). You'll need to cd to that directory before rerunning the challenge program. Good luck!## My solve
**Flag:** `pwn.college{Yrwpm8IrawHrsBmcXySxFlC4vjH.QX4QTN0wCOzAzNzEzW}`

```bash
hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /usr/share/doc/fontconfig directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /
hacker@paths~position-yet-elsewhere:/$ cd /usr/share/doc/fontconfig
hacker@paths~position-yet-elsewhere:/usr/share/doc/fontconfig$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{Yrwpm8IrawHrsBmcXySxFlC4vjH.QX4QTN0wCOzAzNzEzW}
hacker@paths~position-yet-elsewhere:/usr/share/doc/fontconfig$ 

```
Changed my directory to root , and as usr is located in root. invoked the correct path and used the command
## What I learned
Sometimes the shell is hanging out in other directory. U need to change directory and invoke the command using the correct path
## References 
.