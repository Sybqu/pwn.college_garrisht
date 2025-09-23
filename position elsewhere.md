# Position elsewhere
This challenge will require you to execute the /challenge/run program from a specific path (which it will tell you). You'll need to cd to that directory before rerunning the challenge program. Good luck!## My solve
**Flag:** `pwn.college{gHLgLLjsh-Yu-CCxiwFgiOA6dNi.QX3QTN0wCOzAzNzEzW}}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for bash.
```bash
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /etc directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /
hacker@paths~position-elsewhere:/$ cd/etc
bash: cd/etc: No such file or directory
hacker@paths~position-elsewhere:/$ cd etc
hacker@paths~position-elsewhere:/etc$ cd /challenge/run
bash: cd: /challenge/run: Not a directory
hacker@paths~position-elsewhere:/etc$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{gHLgLLjsh-Yu-CCxiwFgiOA6dNi.QX3QTN0wCOzAzNzEzW}
hacker@paths~position-elsewhere:/etc$ 

```

## What I learned
Simillar to previous program!
## References 
.