# Hijacking Commands
Armed with your knowledge, you can now carry out some shenanigans. This challenge is almost the same as the first challenge in this module. Again, this challenge will delete the flag using the rm command. But unlike before, it will not print anything out for you.

How can you solve this? You know that rm is searched for in the directories listed in the PATH variable. You have experience creating the win command when the previous challenge needed it. What else can you create?
**Flag:** pwn.college{kcuzlteN7gnLzYmwFFPK4r3_B3y.QX3cjM1wCOzAzNzEzW}




```bash
hacker@path~hijacking-commands:~$ chmod a+x rm
chmod: cannot access 'rm': No such file or directory
hacker@path~hijacking-commands:~$ chmod a+x see/rm
hacker@path~hijacking-commands:~$ cat rm
cat: rm: No such file or directory
hacker@path~hijacking-commands:~$ cat see/rm
#!/bin/bash
/bin/cat /flag
hacker@path~hijacking-commands:~$ cd see
hacker@path~hijacking-commands:~/see$ PATH="$pwd"
hacker@path~hijacking-commands:~/see$ ./rm
/bin/cat: /flag: Permission denied
hacker@path~hijacking-commands:~/see$ /challenge/run
Trying to remove /flag...
pwn.college{kcuzlteN7gnLzYmwFFPK4r3_B3y.QX3cjM1wCOzAzNzEzW}
hacker@path~hijacking-commands:~/see$ 



```
yeah so the entire time i was setting the PATH incorrectly , then i got the idea of literally decimating the real rm and replacing it with my own :skull:. Imagine how that turned out
## What I learned
Adding commands.
Tedious first time experience but i think i understand it now (trouble troubletroubletrouble)

## References 
Bhumi jtp-1 group-4 :3 (cat fish ahh guy with a cat pfp)
My Mentor My goat :goat: