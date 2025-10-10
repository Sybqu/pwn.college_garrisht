# Executable Shell Scripts
 Make a shellscript that will invoke /challenge/solve, make it executable, and run it without explicitly invoking bash!
**Flag:** pwn.college{IP_Uh-Gw9jBzfrRve8diWkv0luO.QX0cjM1wCOzAzNzEzW}


```bash
hacker@chaining~executable-shell-scripts:~$ touch script.sh
hacker@chaining~executable-shell-scripts:~$ echo /challenge/solve > script.sh
hacker@chaining~executable-shell-scripts:~$ chmod u+rwx script.sh
hacker@chaining~executable-shell-scripts:~$ ./script.sh
Congratulations on your shell script execution! Your flag:
pwn.college{IP_Uh-Gw9jBzfrRve8diWkv0luO.QX0cjM1wCOzAzNzEzW}
hacker@chaining~executable-shell-scripts:~$ 


```
## What I learned
We can run long commands by putting them in a file <called shell script>
and then executing them.
Shell scripts are frequently named with .sh suffix
we can execute by passing it as an argument to a new instance of our shell (bash)
Executing our shell script by making it an executable using "chmod" 
then normally running it like we have been in the past 
## References 
.