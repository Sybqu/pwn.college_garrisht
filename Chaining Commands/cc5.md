# Redirecting Script Output 
In this level, we will practice piping (|) from your script to another program. Like before, you need to create a script that calls the /challenge/pwn command followed by the /challenge/college command, and pipe the output of the script into a single invocation of the /challenge/solve command!
**Flag:** pwn.college{omFy-0LXjJjmM2yZSyYam7yxkkM.QX4ETO0wCOzAzNzEzW}


```bash
hacker@chaining~redirecting-script-output:~$ touch feel.sh
hacker@chaining~redirecting-script-output:~$ echo /challenge/pwn > feel.sh;echo /challenge/college >> feel.sh
hacker@chaining~redirecting-script-output:~$ bash feel.sh | /challenge/solve
Correct! Here is your flag:
pwn.college{omFy-0LXjJjmM2yZSyYam7yxkkM.QX4ETO0wCOzAzNzEzW}
hacker@chaining~redirecting-script-output:~$ 


```
## What I learned
We can run long commands by putting them in a file <called shell script>
and then executing them.
Shell scripts are frequently named with .sh suffix
we can execute by passing it as an argument to a new instance of our shell (bash)
in this way shell takes command from file instead of user.
For shell, our file is still a command so we can use redirectors like we have before
## References 
.