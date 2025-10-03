# Help for builitins
rThis challenge's challenge command is a shell builtin, rather than a program. 
Like before, you need to lookup its help to figure out the secret value to pass to it!
**Flag:**pwn.college{gY6vgbwMxfAoMgKwGt-UGhtZ4O4.QX0ETO0wCOzAzNzEzW}




```bash
hacker@man~help-for-builtins:~$ help /challenge/challenge
bash: help: no help topics match `/challenge/challenge'.  Try `help help' or `man -k /challenge/challenge' or `info /challenge/challenge'.
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!
    
    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "gY6vgbwM".
hacker@man~help-for-builtins:~$ /challenge/challenge --secret gY6vgbwM
bash: /challenge/challenge: No such file or directory
hacker@man~help-for-builtins:~$ challenge --secret gY6vgbwM
Correct! Here is your flag!
pwn.college{gY6vgbwMxfAoMgKwGt-UGhtZ4O4.QX0ETO0wCOzAzNzEzW}

hacker@man~help-for-builtins:~$ 





```
Used the builtin
## What I learned
Using builitins to read documentation instead of man or --help 
## References 
.