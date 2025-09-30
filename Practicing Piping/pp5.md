# Redirecting input
In this level, we will practice using /challenge/run, which will require you to redirect the PWN file to it and have the PWN file contain the value COLLEGE! To write that value to the PWN file, recall the prior challenge on output redirection from echo!


**Flag:**pwn.college{Yz5nwvxe0zLbHKoczh1j4r6L7u3.QXwcTN0wCOzAzNzEzW}







```bash
hacker@piping~redirecting-input:~$ pwn > /challenge/run
bash: /challenge/run: Permission denied
hacker@piping~redirecting-input:~$ /challenge/run > PWN
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ cat pwn
cat: pwn: No such file or directory
hacker@piping~redirecting-input:~$ cat PWN
COLLEGE
hacker@piping~redirecting-input:~$ /challenge/run
You have not redirected anything to my standard input. Please do so, using '<'.
hacker@piping~redirecting-input:~$ echo EGELLOC > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Your PWN file must have the value 'COLLEGE', but I instead read: EGELLOC
hacker@piping~redirecting-input:~$ /challenge/run
You have not redirected anything to my standard input. Please do so, using '<'.
hacker@piping~redirecting-input:~$ echo college >pwn
hacker@piping~redirecting-input:~$ echo college > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Your PWN file must have the value 'COLLEGE', but I instead read: college
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read 
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{Yz5nwvxe0zLbHKoczh1j4r6L7u3.QXwcTN0wCOzAzNzEzW}
hacker@piping~redirecting-input:~$ 

```
From the given example my silly ahh tried typing it backwards because i thought itd be read in reverse like the exmaple but apparently not
## What I learned
Standard output can be redirected to files
This can be done using > character.
File descriptor numbers are communication channels in linux
FD 0
FD 1 
FD 2
standing for standard: input,output and error respectively
hence all these can be redirected to other files.
while errors and outputs are redirected using >
Inputs are redirected using <
## References 
.