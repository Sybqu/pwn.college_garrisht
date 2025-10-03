# Listing processes
renamed /challenge/run to a random filename, and this time made it so that you cannot ls the 
/challenge directory! But I also launched it, so you can find it in the running process list,
 figure out the filename, and relaunch it directly for the flag! Good luck! Use tr -d to remove them!
**flag**:pwn.college{AHeDmwXMVRLKAns1eQnu3ggK3sf.QX4MDO0wCOzAzNzEzW}



```bash
hacker@processes~listing-processes:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.3  0.0   1056   640 ?        Ss   12:48   0:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/do
root           7  0.1  0.0 231708  2560 ?        S    12:48   0:00 /run/dojo/bin/sleep 6h
root         132  0.0  0.0   4132  2560 ?        S    12:48   0:00 /challenge/22719-run-1991
root         135  0.0  0.0   2744  1600 ?        S    12:48   0:00 sleep 6h
hacker       146  0.4  0.0  36972 22080 ?        Sl   12:48   0:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --port 7681 --i
hacker       150  0.0  0.0 231940  4160 pts/0    Ss   12:48   0:00 /run/dojo/bin/bash --login
hacker       160  0.0  0.0 233600  3840 pts/0    R+   12:48   0:00 ps aux
hacker@processes~listing-processes:~$ ps auxww
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.1  0.0   1056   640 ?        Ss   12:48   0:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo/bin/sleep 6h
root           7  0.0  0.0 231708  2560 ?        S    12:48   0:00 /run/dojo/bin/sleep 6h
root         132  0.0  0.0   4132  2560 ?        S    12:48   0:00 /challenge/22719-run-1991
root         135  0.0  0.0   2744  1600 ?        S    12:48   0:00 sleep 6h
hacker       146  0.1  0.0  37072 22080 ?        Sl   12:48   0:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --port 7681 --interface 0.0.0.0 --writable -t disableLeaveAlert true /run/dojo/bin/bash --login
hacker       150  0.0  0.0 231940  4160 pts/0    Ss   12:48   0:00 /run/dojo/bin/bash --login
hacker       161  0.0  0.0 233600  3840 pts/0    R+   12:49   0:00 ps auxww
hacker@processes~listing-processes:~$ /challenge/22719-run-1991
Yahaha, you found me! Here is your flag:
pwn.college{AHeDmwXMVRLKAns1eQnu3ggK3sf.QX4MDO0wCOzAzNzEzW}
Now I will sleep for a while (so that you could find me with 'ps').
```
straightforward :33
## What I learned
listing processes using ps command
by default it lists processes running in terminal
To get more details from ps we need to pass a few arguments
Standard Syntax:
-e for every process
-f for a full format
these can be combined into a singule argument "-ef"
BSD Syntax:
a to list all processes for all users
x to list processes that arent running in the terminal
u for "user-readable" output 
these too ca be combined into a single argument "aux"

## References 
.