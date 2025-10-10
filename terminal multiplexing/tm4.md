# Switching Windows
For this challenge, we've set up a screen session with two windows:

Window 0 has... well, you'll have to switch there to find out!
Window 1 has a welcome message
Attach to the session with screen -r, then use one of the key combinations above to switch to Window 1. Go get that flag!
**Flag:** pwn.college{ETVcgCbdCHiyZL657vRdyO4B2jy.0FO4IDOxwCOzAzNzEzW}




```bash
hacker@terminal-multiplexing~switching-windows:~$ screen -ls
There are screens on:
        144.session_ae1a0f7c0ce2ba72    (Remote or dead)
        150.session_ec551f5bb66c7452    (Remote or dead)
        146.session_ef141ca8ed7b0e33    (Remote or dead)
        150.session_07abe38350a6b2fd    (Remote or dead)
        144.session_c8bd957e93e2eb7c    (Remote or dead)
        147.session_3675d263509b8967    (Remote or dead)
        150.session_fe2aba7f8c5084ad    (Remote or dead)
        135.challenge_session   (Detached)
8 Sockets in /home/hacker/.screen.
hacker@terminal-multiplexing~switching-windows:~$ ^C
hacker@terminal-multiplexing~switching-windows:~$ ^C
hacker@terminal-multiplexing~switching-windows:~$ ^C
hacker@terminal-multiplexing~switching-windows:~$ screen -r 135
[detached from 135.challenge_session]
hacker@terminal-multiplexing~switching-windows:~$ 
hacker@terminal-multiplexing~switching-windows:~$  cat <<MSG
> Excellent work! You found window 0!
> Here is your flag: pwn.college{ETVcgCbdCHiyZL657vRdyO4B2jy.0FO4IDOxwCOzAzNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{ETVcgCbdCHiyZL657vRdyO4B2jy.0FO4IDOxwCOzAzNzEzW}
hacker@terminal-multiplexing~switching-windows:~$ ^C
hacker@terminal-multiplexing~switching-windows:~$ 



```
## What I learned
Detaching and attaching connection
Deatching : Ctrl-A followed by d
Attaching : screen -r
We can list screen sessions using screen -ls
identifiers of sessions are PID of each respective <screen process.name of screen session>
inside a screen session we can have multiple windows and other uses too:
hese windows are handled with different keyboard shortcuts, all starting with Ctrl-A:

Ctrl-A c - Create a new window
Ctrl-A n - Next window
Ctrl-A p - Previous window
Ctrl-A 0 through Ctrl-A 9 - Jump directly to window 0-9
Ctrl-A " - bring up a selection menu of all of the windows
## References 
.