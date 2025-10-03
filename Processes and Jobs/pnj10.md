# Process exit codes     
Launch process in background
**flag**:pwn.college{07XShCGJUnQmMZhpnYvOykWKJGw.QX5YDO1wCOzAzNzEzW}




```bash
hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
114
hacker@processes~process-exit-codes:~$ /challenge/submit-code 114
CORRECT! Here is your flag:
pwn.college{07XShCGJUnQmMZhpnYvOykWKJGw.QX5YDO1wCOzAzNzEzW}
hacker@processes~process-exit-codes:~$ 



```
straightforward :33
## What I learned
Using "?" to get process exit code
0: code fails
1: code succesful
Sometimes an error code that identifies the failure mode
prepend ? with $ to read error code

## References 
.