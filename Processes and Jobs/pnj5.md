# Suspending processes
In this challenge, there's a decoy process that's hogging a critical resource -
 a named pipe (FIFO) at /tmp/flag_fifo into which (like in the Practicing Piping FIFO challenge)
  /challenge/run wants to write your flag. You need to kill this process.
**flag**:pwn.college{8DEuFSFQ8qdnHTqPGf6Xq2Wt73d.QX1QDO0wCOzAzNzEzW}





```bash
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         156     146  0 13:31 pts/0    00:00:00 bash /challenge/run
root         158     156  0 13:31 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can 
background me with Ctrl-Z or, if you're not ready to do that for whatever 
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         156     146  0 13:31 pts/0    00:00:00 bash /challenge/run
root         163     146  0 13:31 pts/0    00:00:00 bash /challenge/run
root         165     163  0 13:31 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{8DEuFSFQ8qdnHTqPGf6Xq2Wt73d.QX1QDO0wCOzAzNzEzW}
hacker@processes~suspending-processes:~$ ^C
hacker@processes~suspending-processes:~$ 

```
## What I learned
Suspending proccess using Ctrl-z

## References 
.