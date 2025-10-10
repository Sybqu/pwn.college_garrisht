# Finding sessions
In this challenge, we've created three screen sessions for you. One of them contains the flag. The other two are decoys!
**Flag:**pwn.college{wLFtk8Wt6YcSy7ZZH2rEKJcu__H.01N4IDOxwCOzAzNzEzW}




```bash
hacker@terminal-multiplexing~finding-sessions:~$ screen -ls
There are screens on:
        144.session_ae1a0f7c0ce2ba72    (Remote or dead)
        150.session_ec551f5bb66c7452    (Remote or dead)
        144.session_e71ef3c4c7850976    (Detached)
        146.session_ef141ca8ed7b0e33    (Detached)
        150.session_07abe38350a6b2fd    (Detached)
5 Sockets in /home/hacker/.screen.
hacker@terminal-multiplexing~finding-sessions:~$ screen -r 146
[detached from 146.session_ef141ca8ed7b0e33]
hacker@terminal-multiplexing~finding-sessions:~$ screen -r 150
Remove dead screens with 'screen -wipe'.
[detached from 150.session_07abe38350a6b2fd]
hacker@terminal-multiplexing~finding-sessions:~$ screen -r 144
Remove dead screens with 'screen -wipe'.
[screen is terminating]
hacker@terminal-multiplexing~finding-sessions:~$ 


hacker@terminal-multiplexing~finding-sessions:~$  echo 'Congratulations! You found the right session!'
Congratulations! You found the right session!
hacker@terminal-multiplexing~finding-sessions:~$  echo pwn.college{wLFtk8Wt6YcSy7ZZH2rEKJcu__H.01N4IDOxwCOzAzNzEzW}
pwn.college{wLFtk8Wt6YcSy7ZZH2rEKJcu__H.01N4IDOxwCOzAzNzEzW}
hacker@terminal-multiplexing~finding-sessions:~$ 



```
## What I learned
Detaching and attaching connection
Deatching : Ctrl-A followed by d
Attaching : screen -r
We can list screen sessions using screen -ls
identifiers of sessions are PID of each respective <screen process.name of screen session>
## References 
.