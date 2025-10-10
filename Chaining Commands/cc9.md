# Scripting With Conditionals
For this challenge, write a script at /home/hacker/solve.sh that:

Takes one argument
If the argument is "pwn", output "college"
For any other input, output nothing
**Flag:**  pwn.college{EW_1r4PIUB5abyEpGOmFt_J5laS.0lNzMDOxwCOzAzNzEzW}


```bash
hacker@chaining~scripting-with-conditionals:~$ echo ' if [ "$1"=="pwn" ] ; then  ;echo "college" ; fi ' >> solve.sh
hacker@chaining~scripting-with-conditionals:~$ cat solve.sh
#!/bin/bash
echo "$1"
 if [ "$1"=="pwn" ] ; then ;echo "output" ; fi 
 if [ "$1"=="pwn" ] ; then  ;echo "college" ; fi 
hacker@chaining~scripting-with-conditionals:~$ echo '#!/bin/bash' > solve.sh;echo 'echo "$1"' >> solve.sh
hacker@chaining~scripting-with-conditionals:~$ echo ' if [ "$1"=="pwn" ] ; then  ; echo "college" ; fi ' >> solve.sh
hacker@chaining~scripting-with-conditionals:~$ ./solve.sh meow
meow
./solve.sh: line 3: syntax error near unexpected token `;'
./solve.sh: line 3: ` if [ "$1"=="pwn" ] ; then  ; echo "college" ; fi '
hacker@chaining~scripting-with-conditionals:~$ echo '#!/bin/bash' > solve.sh;echo 'echo "$1"' >> solve.sh
hacker@chaining~scripting-with-conditionals:~$ echo ' if [ "$1" == "pwn" ] ; then   echo "college" ; fi ' >> solve.sh
hacker@chaining~scripting-with-conditionals:~$ ./solve.sh meow
meow
hacker@chaining~scripting-with-conditionals:~$ /challenge/run
Test failed for input 'pwn'
Expected: 'college'
Got: 'pwn
college'
hacker@chaining~scripting-with-conditionals:~$ 
hacker@chaining~scripting-with-conditionals:~$ cat solve.sh
#!/bin/bash
echo "$1"
 if [ "$1" == "pwn" ] ; then   echo "college" ; fi 
hacker@chaining~scripting-with-conditionals:~$ ^C
hacker@chaining~scripting-with-conditionals:~$ ^C
hacker@chaining~scripting-with-conditionals:~$ echo '#!/bin/bash' > solve.sh >> solve.sh
hacker@chaining~scripting-with-conditionals:~$ echo ' if [ "$1" == "pwn" ] ; then   echo "college" ; fi ' >> solve.sh
hacker@chaining~scripting-with-conditionals:~$ ./solve.sh meww
hacker@chaining~scripting-with-conditionals:~$ ./solve.sh pwn
college
hacker@chaining~scripting-with-conditionals:~$ /challenge/run
Correct! Your script properly handles all the conditions.
Here's your flag:
pwn.college{EW_1r4PIUB5abyEpGOmFt_J5laS.0lNzMDOxwCOzAzNzEzW}
hacker@chaining~scripting-with-conditionals:~$ 


```
Bit of an output issue but nothing much (ragebait)
## What I learned
We can modify shell scripts to accept arguments. This makes them more useful
The script can access these arguments using special variables:

$1 contains the first argument
$2 the second argument
and so on..
## References 
pwn college documentation