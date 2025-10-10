# Launching screen
For this challenge, you'll need to:

Launch screen
Detach from it.
Run /challenge/run (this will secretly send the flag to your detached session!)
Reattach to see your prize
**Flag:**pwn.college{0-ln2nvCzG7ouLcq_UrvVa_G3KI.0VN4IDOxwCOzAzNzEzW}



```bash
hacker@terminal-multiplexing~detaching-and-attaching:~$ screen
[detached from 147.pts-0.terminal-multiplexing~detaching-and-attaching]
hacker@terminal-multiplexing~detaching-and-attaching:~$ /challenge/run
Found detached screen session: 147.pts-0.terminal-multiplexing~detaching-and-attaching
Sending flag to your screen session...

Flag sent! Now reattach to your screen session with:

  screen -r

You'll find the flag waiting for you there!
hacker@terminal-multiplexing~detaching-and-attaching:~$ screen -r
[screen is terminating]
hacker@terminal-multiplexing~detaching-and-attaching:~$ 

hacker@terminal-multiplexing~detaching-and-attaching:~$ echo Yes! Flag is: pwn.college{EHA_iMb4WpoCCNXVZJhWz2yf2nU.0lN4IDOxwCOzAzNzEzW}
Yes! Flag is: pwn.college{EHA_iMb4WpoCCNXVZJhWz2yf2nU.0lN4IDOxwCOzAzNzEzW}
hacker@terminal-multiplexing~detaching-and-attaching:~$


```
## What I learned
Detaching and attaching connection
Deatching : Ctrl-A followed by d
Attaching : screen -r
## References 
.