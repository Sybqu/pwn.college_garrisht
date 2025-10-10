# Scripting With Arguments
For this challenge, you need to write a script at /home/hacker/solve.sh that:
Takes two arguments
Outputs them in REVERSE order (second argument first, then the first argument)
**Flag:**  pwn.college{kJjqj8lZ5D8wSmHZRssEllLTOPT.0VNzMDOxwCOzAzNzEzW}

```bash
hacker@chaining~scripting-with-arguments:~$ touch solve.sh
hacker@chaining~scripting-with-arguments:~$ echo '#!/bin/bash' > solve.sh;echo 'echo "Sec arg: $2"' >> solve.sh;echo 'echo "fir arg:$1"' >> solve.sh
hacker@chaining~scripting-with-arguments:~$ chmod u+rwx solve.sh
hacker@chaining~scripting-with-arguments:~$ ./solve.sh
Sec arg: 
fir arg:
hacker@chaining~scripting-with-arguments:~$ solve.sh rahahaha meow
bash: solve.sh: command not found
hacker@chaining~scripting-with-arguments:~$ ./solve.sh rahaha meow
Sec arg: meow
fir arg:rahaha
hacker@chaining~scripting-with-arguments:~$ /challenge/run
Not quite right!
Expected: college_2FV2EErebCU pwn_FDwsJvGzYQ
Got: Sec arg: college_2FV2EErebCU
fir arg:pwn_FDwsJvGzYQ
hacker@chaining~scripting-with-arguments:~$ echo '#!/bin/bash' > solve.sh;echo 'echo "Sec arg: $2" echo "fir arg:$1"' >> solve.sh
hacker@chaining~scripting-with-arguments:~$ ./solve.sh meow haii
Sec arg: haii echo fir arg:meow
hacker@chaining~scripting-with-arguments:~$ /challenge/run
Not quite right!
Expected: college_ATwvaeQnnO0 pwn_gztdMYSWTBg
Got: Sec arg: college_ATwvaeQnnO0 echo fir arg:pwn_gztdMYSWTBg
hacker@chaining~scripting-with-arguments:~$ echo '#!/bin/bash' > solve.sh;echo 'echo "$2" echo "$1"' >> solve.sh
hacker@chaining~scripting-with-arguments:~$ ./solve.sh meow ee
ee echo meow
hacker@chaining~scripting-with-arguments:~$ echo '#!/bin/bash' > solve.sh;echo 'echo "$2" "$1"' >> solve.sh
hacker@chaining~scripting-with-arguments:~$ /challenge/run
Correct! Your script properly reversed the arguments.
Here's your flag:
pwn.college{kJjqj8lZ5D8wSmHZRssEllLTOPT.0VNzMDOxwCOzAzNzEzW}
hacker@chaining~scripting-with-arguments:~$ 


```
Bit of an output issue but nothing much
## What I learned
We can modify shell scripts to accept arguments. This makes them more useful
The script can access these arguments using special variables:

$1 contains the first argument
$2 the second argument
and so on..
## References 
pwn college documentation