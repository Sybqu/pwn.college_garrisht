# multi-word variables
 In this level, you'll need to set the variable PWN to COLLEGE YEAH.
**Flag:**pwn.college{IM57rIn41yEd70pNKTfadoba8AA.QXwYTN0wCOzAzNzEzW}





```bash
hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{IM57rIn41yEd70pNKTfadoba8AA.QXwYTN0wCOzAzNzEzW}
hacker@variables~multi-word-variables:~$ 
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

## References 
.