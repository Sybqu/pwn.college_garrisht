# Reading input
In this challenge, your job is to use read to set the PWN variable to the value COLLEGE. 

**flag**:pwn.college{Q_JVSWZZ_PMdVq7PUJjYsDLjTpV.QX4cTN0wCOzAzNzEzW}



```bash
hacker@variables~reading-input:~$ read PWN
COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{Q_JVSWZZ_PMdVq7PUJjYsDLjTpV.QX4cTN0wCOzAzNzEzW}
hacker@variables~reading-input:~$ echo $PWN
COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{Q_JVSWZZ_PMdVq7PUJjYsDLjTpV.QX4cTN0wCOzAzNzEzW}
hacker@variables~reading-input:~$ 



```
used man env to get to know more about it . Apparently its supposed to run a program in a modfied environment
## What I learned
User input can be read using `read` builtin. It reads input into a variable. 
Here we use "-p" argument which lets us specify a prompt
"Read" reads data from out standard input
## References 
.