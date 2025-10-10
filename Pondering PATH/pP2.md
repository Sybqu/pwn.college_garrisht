# setting PATH
Let's practice. This level's /challenge/run will run the win command via its bare name, but this
 command exists in the /challenge/more_commands/ directory, which is not initially in the PATH. 
 The win command is the only thing that /challenge/run needs, so you can just overwrite PATH with
  that one directory. Good luck!
**Flag:**pwn.college{c2CkOfo5HnvfR8mWXQN7hMDecYd.QX1cjM1wCOzAzNzEzW}






```bash
hacker@path~setting-path:~$ PATH=~/challenge/more_commands/
hacker@path~setting-path:~$ /challenge/run
Invoking 'win'....
/challenge/run: line 4: win: command not found
It looks like that did not work... Did you set PATH correctly?
hacker@path~setting-path:~$ ls
bash: ls: command not found
hacker@path~setting-path:~$ PATH = /challenge/more_commands/
bash: PATH: command not found
hacker@path~setting-path:~$ PATH=/challenge/more_commands/
hacker@path~setting-path:~$ /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{c2CkOfo5HnvfR8mWXQN7hMDecYd.QX1cjM1wCOzAzNzEzW}
hacker@path~setting-path:~$ 


```
## What I learned
Special Shell Variable : PATH 
it stores a bunch of directory paths in which shell will search for programs corresponding to commands.
We can use custom scripts just by their name by adding their paths to the PATH variable
## References 
.