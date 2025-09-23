# Position thy self
This challenge will require you to execute the /challenge/run program from a specific path (which it will tell you).
## My solve
**Flag:** pwn.college{McjPxBnK0v9AQafDoJmE-WDEnaZ.QX2QTN0wCOzAzNzEzW}

```bash
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /var/lib/apt/lists directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ /var/lib/apt/lists
bash: /var/lib/apt/lists: Is a directory
hacker@paths~position-thy-self:~$ cd /car/lib/apt/lists
bash: cd: /car/lib/apt/lists: No such file or directory
hacker@paths~position-thy-self:~$ cd root
bash: cd: root: No such file or directory
hacker@paths~position-thy-self:~$ cd /
hacker@paths~position-thy-self:/$ cd /var/lib/apt/lists
hacker@paths~position-thy-self:/var/lib/apt/lists$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{McjPxBnK0v9AQafDoJmE-WDEnaZ.QX2QTN0wCOzAzNzEzW}
hacker@paths~position-thy-self:/var/lib/apt/lists$ 

```
Ran the command.
It told me the correct path
Changed directory to root 
then opened lists directory using the "Cd" command
once in the correct path i ran the required command giving me the flag
## What I learned
cd command can be used to change directories. Each process has a directory in which it is running
The terminal shows me via "~" what my path shell is located at.
## References 
.