# Exclusionary Globbing
go forth to /challenge/files and run /challenge/run with all files that don't start with p, w, or n!

**Flag:**pwn.college{Yv9Dfm4uObN6clyhKL_WzpXOu7r.QX2IDO0wCOzAzNzEzW}






```bash
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]
Your expansion did not expand to the requested files (amazing beautiful 
challenging delightful educational fantastic great happy incredible jovial kind 
laughing magical optimistic queenly radiant splendid thrilling uplifting 
victorious xenial youthful zesty).
Instead, it expanded to:
[!pwn]
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{Yv9Dfm4uObN6clyhKL_WzpXOu7r.QX2IDO0wCOzAzNzEzW}
hacker@globbing~exclusionary-globbing:/challenge/files$ 

```
ez
## What I learned
basically using a not statement!


## References 
.