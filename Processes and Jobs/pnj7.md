# Backgrounding processes
This level's run wants to see another copy of itself running, not suspended, and using the same terminal. 
**flag**:pwn.college{gAChTqsUW_2Mos3gi5YfvLZfgjW.QX3QDO0wCOzAzNzEzW}


```bash
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         177 S+   bash /challenge/run
root         179 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the 
background, and then launch a new version of me! You can background me with 
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to 
do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~backgrounding-processes:~$ 


Yay, I'm now running the background! Because of that, this text will probably 
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times 
to scroll this text out.

hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         177 S    bash /challenge/run
root         187 S    sleep 6h
root         188 S+   bash /challenge/run
root         190 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{gAChTqsUW_2Mos3gi5YfvLZfgjW.QX3QDO0wCOzAzNzEzW}
hacker@processes~backgrounding-processes:~$ 

```
straightforward :33
## What I learned
Suspending an active process via ctrl-z
holding ctrl then pressing z.
The fg builtin command can be used to resumes suspended processes and puts them in foreground of our terminal.
The bg builtin command can be used to put a process to background of our terminal.

## References 
.