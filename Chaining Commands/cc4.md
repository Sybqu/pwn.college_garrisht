# Your First Shell Script
Now, it's your turn! Same as last level, run /challenge/pwn and then /challenge/college, but this time in a shell script called x.sh, then run it with bash!
**Flag:** pwn.college{0JIKIfnreSclZoKBOaUInMegqNY.QXxcDO0wCOzAzNzEzW}
`


```bash
hacker@chaining~your-first-shell-script:~$ touch x.sh
hacker@chaining~your-first-shell-script:~$ echo /challenge/pwn > x.sh;echo /challenge/college >> x.sh
hacker@chaining~your-first-shell-script:~$ bash x.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{0JIKIfnreSclZoKBOaUInMegqNY.QXxcDO0wCOzAzNzEzW}
hacker@chaining~your-first-shell-script:~$ 

```
## What I learned
We can run long commands by putting them in a file <called shell script>
and then executing them.
Shell scripts are frequently named with .sh suffix
we can execute by passing it as an argument to a new instance of our shell (bash)
in this way shell takes command from file instead of user.
## References 
.