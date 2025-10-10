# Switching windows tmux
We've created a tmux session with two windows:

Window 0 has the flag!
Window 1 has your warm welcome.
Go get that flag!
**Flag:** pwn.college{wlF84HiZYHINXcrsRTkRnmRXOLe.0FM5IDOxwCOzAzNzEzW}




```bash
hacker@terminal-multiplexing~switching-windows-tmux:~$  cat <<MSG
> Excellent work! You found window 0!
> Here is your flag: pwn.college{wlF84HiZYHINXcrsRTkRnmRXOLe.0FM5IDOxwCOzAzNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{wlF84HiZYHINXcrsRTkRnmRXOLe.0FM5IDOxwCOzAzNzEzW}
hacker@terminal-multiplexing~switching-windows-tmux:~$ 


```
## What I learned
tmux: "Im the upgrade" <the boys ref btw>
tmux uses ctrl-a instead of ctrl-b as command prefix
ctrl-b + d : Dettach
The commands also differ:

tmux ls - List sessions
tmux attach or tmux a - Reattach to session
More commands:
Ctrl-B c - Create a new window
Ctrl-B n - Next window
Ctrl-B p - Previous window
Ctrl-B 0 through Ctrl-B 9 - Jump to window 0-9
Ctrl-B w - See a nice window picker
Tmux shows your windows at the bottom in a status bar 
"*" shows your current window
## References 
.