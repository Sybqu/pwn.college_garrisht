# exporting variables
 n this challenge, you must invoke /challenge/run with the PWN variable exported and set to the value COLLEGE, and the COLLEGE variable set to the value PWN but not exported
**Flag:**pwn.college{sFQ2X9opiqhoL5YKkuBva0dzLTm.QXyYTN0wCOzAzNzEzW}






```bash
hacker@variables~exporting-variables:~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run PWN
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great 
job! Here is your flag:
pwn.college{sFQ2X9opiqhoL5YKkuBva0dzLTm.QXyYTN0wCOzAzNzEzW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ 


```
checking stuff out!
## What I learned
= is used as an assignment operator to set variables
Spaces arent allowed for eg:
VAR=12312 is valid
VAR = 12312 is not valid as shell will try to run the "var" command
also $VAR is not used because $ is only used to access variables.
$ triggers variable expansion...which...can..lead..to..vulnerabilities...:skull:
Spaces have special signifiance and there are places that they cannot be used liberally.
When shell sees "<SPACE>" it ends variable assignment and interprets the next word as a command, hence variable names need to be quoted if we wanna assign a multi-word variable
Variables in shell session are local to that shell process.
Shell variables are not exported by default hence to export them the 

# Export command needs to be used

## References 
.