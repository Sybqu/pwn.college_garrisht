# Starting background processes
Launch process in background
**flag**:pwn.college{oRILv_xrRBK7VdqSiQwK-_1K7PJ.QX5QDO0wCOzAzNzEzW}



```bash
hacker@processes~starting-backgrounded-processes:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.1  0.0   1056   640 ?        Ss   19:20   0:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/do
root           7  0.1  0.0 231708  2560 ?        S    19:20   0:00 /run/dojo/bin/sleep 6h
hacker       132  0.1  0.0  36972 21440 ?        Sl   19:21   0:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --port 7681 --i
hacker       136  0.0  0.0 231940  4160 pts/0    Ss   19:21   0:00 /run/dojo/bin/bash --login
hacker       146  0.0  0.0 233600  3840 pts/0    R+   19:21   0:00 ps aux
hacker@processes~starting-backgrounded-processes:~$ /challenge/run
You've started me in the foreground! You must start me in the background (by 
appending '&' to the command) to get the flag!
hacker@processes~starting-backgrounded-processes:~$ /challenge/run &
[1] 150
hacker@processes~starting-backgrounded-processes:~$ 


Yay, you started me in the background! Because of that, this text will probably 
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{oRILv_xrRBK7VdqSiQwK-_1K7PJ.QX5QDO0wCOzAzNzEzW}



```
straightforward :33
## What I learned
Suspending an active process via ctrl-z
holding ctrl then pressing z.
The fg builtin command can be used to resumes suspended processes and puts them in foreground of our terminal.
The bg builtin command can be used to put a process to background of our terminal.
Using "&" to launch a process in background.


## References 
.