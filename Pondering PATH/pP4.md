# Adding commands
Previously, the win command that /challenge/run executed was stored in /challenge/more_commands. This time, win does not exist! Recall the final level of Chaining Commands, and make a shell script called win, add its location to the PATH, and enable /challenge/run to find it!
**Flag:** pwn.college{wNwq4cCz9VfEuhVSJoIQDbnsvkx.QX2cjM1wCOzAzNzEzW}




```bash
hacker@path~adding-commands:~$ cd seeuh
hacker@path~adding-commands:~/seeuh$ touch win
hacker@path~adding-commands:~/seeuh$ echo '#!/bin/bash' > code
hacker@path~adding-commands:~/seeuh$ echo '#!/bin/bash' > win
hacker@path~adding-commands:~/seeuh$ echo '$(/bin/cat /flag)' >> win
hacker@path~adding-commands:~/seeuh$ chmod a+x ~/seeuh/win
hacker@path~adding-commands:~/seeuh$ cd /
hacker@path~adding-commands:/$ ~/seeuh/win
/bin/cat: /flag: Permission denied
hacker@path~adding-commands:/$ PATH="~/seeuh/win"
hacker@path~adding-commands:/$ /challenge/run
Invoking 'win'....
/challenge/run: line 4: win: command not found
It looks like that did not work... Did you set PATH correctly?
hacker@path~adding-commands:/$ ^C
hacker@path~adding-commands:/$ PATH="~/seeuh"
hacker@path~adding-commands:/$ /challenge/run
Invoking 'win'....
/home/hacker/seeuh/win: line 2: pwn.college{wNwq4cCz9VfEuhVSJoIQDbnsvkx.QX2cjM1wCOzAzNzEzW}: command not found
It looks like that did not work... Did you set PATH correctly?
hacker@path~adding-commands:/$ ^C
hacker@path~adding-commands:/$ 



```
SKULL It somehow gave me the flag :skull: but still ima spend more time to see where i went wrong
## What I learned
Adding commands.
Tedious first time experience but i think i understand it now

## References 
.