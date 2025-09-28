# Tab completion
This challenge has copied the flag into /challenge/pwncollege, and you can freely cat that file. But you can't type the filename: we used some serious trickery to make sure that you must tab-complete it. 

**Flag:**pwn.college{gmLHI0F4mezZ1qCDUcA2839pW2B.0FN0EzNxwCOzAzNzEzW}






```bash
hacker@globbing~tab-completion:~$ ls /challenge
DESCRIPTION.md  pwncollege​
hacker@globbing~tab-completion:~$ cat /challenge/pwn<TAB>
bash: syntax error near unexpected token `newline'
hacker@globbing~tab-completion:~$ cat /challenge/pwn<TAB>
bash: syntax error near unexpected token `newline'
hacker@globbing~tab-completion:~$ cat /challenge
cat: /challenge: Is a directory
hacker@globbing~tab-completion:~$ cd /challenge
hacker@globbing~tab-completion:/challenge$ cat pwn<TAB>
bash: syntax error near unexpected token `newline'
hacker@globbing~tab-completion:/challenge$ ^C
hacker@globbing~tab-completion:/challenge$ cat p<tab>
bash: syntax error near unexpected token `newline'
hacker@globbing~tab-completion:/challenge$ ^C
hacker@globbing~tab-completion:/challenge$ cat pwncollege​ 
pwn.college{gmLHI0F4mezZ1qCDUcA2839pW2B.0FN0EzNxwCOzAzNzEzW}
hacker@globbing~tab-completion:/challenge$ 

Yeah, i know you know where i went wrong

```

## What I learned
tab spam~~~~~~~
auto completion
using * can lead to unintentional errors.


## References 
.