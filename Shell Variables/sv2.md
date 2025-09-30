# setting variables
Have your shell print out the FLAG variable and solve this challenge!
**Flag:**pwn.college{QJrDt9XMNCcripGi1s2K0RBFlyN.QX5UTN0wCOzAzNzEzW}




```bash
hacker@variables~printing-variables:~$ echo PWD
hacker@variables~setting-variables:~$ PWN=COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{QJrDt9XMNCcripGi1s2K0RBFlyN.QX5UTN0wCOzAzNzEzW}
hacker@variables~setting-variables:~$ 


```
checking stuff out!
## What I learned
= is used as an assignment operator to set variables
Spaces arent allowed for eg:
VAR=12312 is valid
VAR = 12312 is not valid as shell will try to run the "var" command
also $VAR is not used because $ is only used to access variables.
$ triggers variable expansion...which...can..lead..to..vulnerabilities...:skull:

## References 
.