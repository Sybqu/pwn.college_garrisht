# Detaching and attaching tmux
For this challenge:

Launch tmux
Detach from it.
Run /challenge/run (this will send the flag to your detached session!)
Reattach to see your prize
**Flag:** pwn.college{YQ3CKGIAGQVLNSJ6ydNOqYevoSF.0VO4IDOxwCOzAzNzEzW}




```bash
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux
[detached (from session 0)]
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ /challenge/run
Found detached tmux session: 0
Sending flag to your tmux session...

Flag sent! Now reattach to your tmux session with:
  tmux attach

You'll find the flag waiting for you there!
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux a
[detached (from session 0)]
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ 
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$  echo Congratulations, here is your flag: pwn.college{YQ3CKGIAGQVLNSJ6ydNOqYevoSF.0VO4IDOxwCOzAzNzEzW}
Congratulations, here is your flag: pwn.college{YQ3CKGIAGQVLNSJ6ydNOqYevoSF.0VO4IDOxwCOzAzNzEzW}
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ 



```
## What I learned
tmux: "Im the upgrade" <the boys ref btw>
tmux uses ctrl-a instead of ctrl-b as command prefix
ctrl-b + d : Dettach
The commands also differ:

tmux ls - List sessions
tmux attach or tmux a - Reattach to session
## References 
.