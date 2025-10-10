# The SUID bit
Now, we are going to let you add the SUID bit to the /challenge/getroot program in order to spawn a root shell for you to cat the flag yourself!
  **Flag:**pwn.college{szrIhIiJPjRCfxYRPrrdQqCxzEf.QXzEjN0wCOzAzNzEzW}


`

```bash
hacker@permissions~the-suid-bit:~$ chmod u+s /challenge/getroot
hacker@permissions~the-suid-bit:~$ catt /flag
bash: catt: command not found
hacker@permissions~the-suid-bit:~$ cat /flag
cat: /flag: Permission denied
hacker@permissions~the-suid-bit:~$ /challenge/getroot
SUCCESS! You have set the suid bit on this program, and it is running as root! 
Here is your shell...
root@permissions~the-suid-bit:~# cat /flag
pwn.college{szrIhIiJPjRCfxYRPrrdQqCxzEf.QXzEjN0wCOzAzNzEzW}
root@permissions~the-suid-bit:~# 


```
straight fwd c
## What I learned
SUID command
 the "Set User ID" (SUID) permissions bit allows the user to run a program as the owner of that program's file.

 e.g
 ```
  hacker@dojo:~$ ls -l /usr/bin/sudo
-rwsr-xr-x 1 root root 232416 Dec 1 11:45 /usr/bin/sudo
hacker@dojo:~$

```
s part in place of executable bit means program is executable with SUID
The program executes as the owner user.
SUID bit can be set using chmod
## References 
. 