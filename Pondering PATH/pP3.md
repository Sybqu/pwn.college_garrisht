# Finding commands
In this challenge, we added a win command somewhere in your $PATH,
 but it won't give you the flag. Instead, it's in the same directory 
 as a flag file that we made readable by you! You must find win (with the which command),
  and cat the flag out of that directory!
**Flag:**pwn.college{EfvnQVWXY4OSXSWcY0SrUrTGmGk.01NzEzNxwCOzAzNzEzW}







```bash
hacker@path~finding-commands:~$ which flag
which: no flag in (/run/challenge/bin:/run/dojo/bin:/bin:/challenge/paths/5397:/challenge/paths/6416:/challenge/paths/30628:/challenge/paths/13320:/challenge/paths/3570:/challenge/paths/18186:/challenge/paths/239:/challenge/paths/28061:/challenge/paths/1662:/challenge/paths/30647:/challenge/paths/6261:/challenge/paths/27379:/challenge/paths/4235:/challenge/paths/17370:/challenge/paths/8240:/challenge/paths/26087:/challenge/paths/17624:/challenge/paths/31782:/challenge/paths/10348:/challenge/paths/19660:/challenge/paths/9138:/challenge/paths/8997:/challenge/paths/4932:/challenge/paths/29543:/challenge/paths/6134:/challenge/paths/8677:/challenge/paths/19671:/challenge/paths/20334:/challenge/paths/31847:/challenge/paths/30063:/challenge/paths/20455:/challenge/paths/20091:/challenge/paths/5390:/challenge/paths/22280:/challenge/paths/2706:/challenge/paths/2359:/challenge/paths/8243:/challenge/paths/32642:/challenge/paths/24676:/challenge/paths/31338:/challenge/paths/31952:/challenge/paths/30526:/challenge/paths/5464:/challenge/paths/26665:/challenge/paths/6324:/challenge/paths/4479:/challenge/paths/12704:/challenge/paths/5647:/challenge/paths/25897:/challenge/paths/28211:/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin)
hacker@path~finding-commands:~$ which win
/challenge/paths/30526/win
hacker@path~finding-commands:~$ ^C
hacker@path~finding-commands:~$ cat /challenge/paths/30526/win
#!/bin/bash

/bin/fold -s <<< "Search for the flag in the same directory in which I am located!"
hacker@path~finding-commands:~$  /challenge/paths/30526/win
Search for the flag in the same directory in which I am located!
hacker@path~finding-commands:~$  /challenge/paths/30526/win /flag
Search for the flag in the same directory in which I am located!
hacker@path~finding-commands:~$ which  /challenge/paths/30526/win /flag
/challenge/paths/30526/win
which: no flag in ()
hacker@path~finding-commands:~$ cd  /challenge/paths/30526/win 
bash: cd: /challenge/paths/30526/win: Not a directory
hacker@path~finding-commands:~$ /challenge/paths/30526/win/flag
bash: /challenge/paths/30526/win/flag: Not a directory
hacker@path~finding-commands:~$ cat /challenge/paths/30526/win/flag
cat: /challenge/paths/30526/win/flag: Not a directory
hacker@path~finding-commands:~$ grep pwn.college  /challenge/paths/30526/win 
hacker@path~finding-commands:~$ grep pwn.college /challenge/paths/30526/win
hacker@path~finding-commands:~$ ^C
hacker@path~finding-commands:~$ cat /challenge/paths/30526/flag
pwn.college{EfvnQVWXY4OSXSWcY0SrUrTGmGk.01NzEzNxwCOzAzNzEzW}
hacker@path~finding-commands:~$ 


```
## What I learned
which command: used to search for paths where the commands are stored.
Mirrors the shell searching process
## References 
.