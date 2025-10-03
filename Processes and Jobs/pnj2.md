# Listing processes
In this challenge, /challenge/run will refuse to run while /challenge/dont_run is running! You must find the dont_run process and kill it. If you fail, pwn.college will disavow all knowledge of your mission. 
**flag**:pwn.college{ApH45y0rtjVxv3-qE_1_BcvO7MP.QXyQDO0wCOzAzNzEzW}




```bash
hacker@processes~killing-processes:~$ /challenge/run
Nope! /challenge/dont_run is still running! You gotta terminate it before I 
give you the flag!
hacker@processes~killing-processes:~$ ps aux | grep dont_run
hacker       136  0.0  0.0 231576  3520 ?        Ss   12:56   0:00 /challenge/dont_run
hacker       167  0.0  0.0 230696  2560 pts/0    S+   12:59   0:00 grep --color=auto dont_run
hacker@processes~killing-processes:~$ kill 136
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{ApH45y0rtjVxv3-qE_1_BcvO7MP.QXyQDO0wCOzAzNzEzW}
hacker@processes~killing-processes:~$ ^C
hacker@processes~killing-processes:~$ 
```
straightforward :33
## What I learned
killing a process via the <kill> command.
syntax: kill PID
we can grab the pid via the ps command

## References 
.