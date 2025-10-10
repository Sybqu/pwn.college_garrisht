# Understanding Shebangs
For this challenge, create a script at /home/hacker/solve.sh that has a proper shebang and outputs "hack the planet". Remember to make it executable, then run /challenge/run to verify your script works correctly!
**Flag:**  pwn.college{ckTLT1jKEiSsIFIEUcx05EGQBYa.0VOzMDOxwCOzAzNzEzW}

```bash
hacker@chaining~understanding-shebangs:~$ echo #!/bin/bash > solve.sh;echo echo "hack the planet" >> solve.sh

hacker@chaining~understanding-shebangs:~$ ^C
hacker@chaining~understanding-shebangs:~$ echo '#!/bin/bash' >
 solve.sh;echo'echo "hack the planet"' >> solve.sh
bash: echoecho "hack the planet": command not found
hacker@chaining~understanding-shebangs:~$ echo '#!/bin/bash' > solve.sh;echo 'echo "hack the planet"' >> solve.sh
hacker@chaining~understanding-shebangs:~$ /challenge/run
Testing your script...
Perfect! Your flag:
Flag: pwn.college{ckTLT1jKEiSsIFIEUcx05EGQBYa.0VOzMDOxwCOzAzNzEzW}

hacker@chaining~understanding-shebangs:~$ 

```
forgot quoting arguments led to timewaste :c
## What I learned
When a program is invoked in Linux, the Linux kernel first inspects the file to determine how it should be run.
 This does NOT use the extension (which is why you don't have to name your shell scripts with a .sh extension,
  or your Python scripts with a .py extension, or so on). Rather, Linux looks at the first few bytes of the file
   for this information.

There are a bunch of different types of programs, but if the program file starts with the characters
 #! (often termed a "shebang"), Linux treats the file as an interpreted program, and the contents of 
 the rest of the line as the path to the interpreter. It then invokes the interpreter with the path to
  the program file as its only argument.
## References 
pwn college documentation