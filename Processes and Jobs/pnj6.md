# Resuming processes
Try it here! /challenge/run will refuse to give you the flag until you interrupt it
**flag**:pwn.college{cybT9zQNKkDEkzlNWckRqj7EYTf.QX2QDO0wCOzAzNzEzW}





```bash
hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with 
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg
/challenge/run
I'm back! Here's your flag:
pwn.college{cybT9zQNKkDEkzlNWckRqj7EYTf.QX2QDO0wCOzAzNzEzW}
Don't forget to press Enter to quit me!

Goodbye!
hacker@processes~resuming-processes:~$ 


```
straightforward :33
## What I learned
Suspending an active process via ctrl-z
holding ctrl then pressing z.
The fg builtin command can be used to resumes suspended processes and puts them in foreground of our terminal

## References 
.