# the PATH variable (Time to ponder again)
In this level, you will disrupt the operation of the /challenge/run program. This program will DELETE the flag file using the rm command. However, if it can't find the rm command, the flag will not be deleted, and the challenge will give it to you! Thus, you must make it so that /challenge/run also can't find the rm command!
**Flag:**pwn.college{cZwfc98OlJhOnJAD_w0d5lmn35G.QX2cDM1wCOzAzNzEzW}





```bash
hacker@path~the-path-variable:~$ rm
rm: missing operand
Try 'rm --help' for more information.
hacker@path~the-path-variable:~$ PATH =""
bash: PATH: command not found
hacker@path~the-path-variable:~$ rm
rm: missing operand
Try 'rm --help' for more information.
hacker@path~the-path-variable:~$ rm PATH=""
rm: cannot remove 'PATH=': No such file or directory
hacker@path~the-path-variable:~$ rm
rm: missing operand
Try 'rm --help' for more information.
hacker@path~the-path-variable:~$ PATH=""
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{cZwfc98OlJhOnJAD_w0d5lmn35G.QX2cDM1wCOzAzNzEzW}
hacker@path~the-path-variable:~$ 

```
## What I learned
Special Shell Variable : PATH 
it stores a bunch of directory paths in which shell will search for programs corresponding to commands.
## References 
.