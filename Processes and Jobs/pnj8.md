# Foregrounding processes
Follow instructions
**flag**:pwn.college{Ea1yx7eeYHe-O6v5EF7HA0W5rn9.QX4QDO0wCOzAzNzEzW}


```bash
hacker@processes~foregrounding-processes:~$ /challenge/run
To pass this level, you need to suspend me, resume the suspended process in the 
background, and *then* foreground it without re-suspending it! You can 
background me with Ctrl-Z (and resume me in the background with 'bg') or, if 
you're not ready to do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~foregrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~foregrounding-processes:~$ 


Yay, I'm now running the background! Because of that, this text will probably 
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times 
to scroll this text out. After that, resume me into the foreground with 'fg'; 
I'll wait.

hacker@processes~foregrounding-processes:~$ fg
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!

pwn.college{Ea1yx7eeYHe-O6v5EF7HA0W5rn9.QX4QDO0wCOzAzNzEzW}
hacker@processes~foregrounding-processes:~$ 

```
straightforward :33
## What I learned
Suspending an active process via ctrl-z
holding ctrl then pressing z.
The fg builtin command can be used to resumes suspended processes and puts them in foreground of our terminal.
The bg builtin command can be used to put a process to background of our terminal.

## References 
.