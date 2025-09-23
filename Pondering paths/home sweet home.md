# home sweet home
Write a path with following constraints
## My solve
**Flag:** pwn.college{4-lwgSUoPG7m_T5vMn1jTYlaBQB.QXzMDO0wCOzAzNzEzW}

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for bash.
```bash
hacker@paths~home-sweet-home:~$ cd /
hacker@paths~home-sweet-home:/$ /challenge/run ~/a
Writing the file to /home/hacker/a!
... and reading it back to you:
pwn.college{4-lwgSUoPG7m_T5vMn1jTYlaBQB.QXzMDO0wCOzAzNzEzW}
hacker@paths~home-sweet-home:/$ 

```
changed to root, invoked the challenge/run command with the path "~/a~" a is the name of a file and "~" stands for home directory
## What I learned
By default shell hangouts at "~" because most of the time will be spent in home directory. Hence whenever bash sees "~" it will expand to our home directory"~" is the expansion of an absolute path.
## References 
.