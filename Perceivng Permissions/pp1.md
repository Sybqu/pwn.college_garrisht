# changing file owner 
in this level, we will practice changing the owner of the /flag file to the hacker user, and then read the flag. For this challenge only, I made it so that you can use chown to your heart's content as the hacker user (again, typically, this requires you to be root). Use this power wisely and chown away!
**Flag:**pwn.college{QazchC-K_NOEjmCSg8SPmNhTgco.QXxEjN0wCOzAzNzEzW}
`

```bash
hacker@permissions~changing-file-ownership:~$ ls
1        PWN  f             myflag        pwn
COLLEGE  a    flag_fifo     not-the-flag  the-flag
Desktop  ae   instructions  not-the0flag
hacker@permissions~changing-file-ownership:~$ cat flag
cat: flag: No such file or directory
hacker@permissions~changing-file-ownership:~$ cat /flag
cat: /flag: Permission denied
hacker@permissions~changing-file-ownership:~$ chown hacker /flag
hacker@permissions~changing-file-ownership:~$ cat /flag
pwn.college{QazchC-K_NOEjmCSg8SPmNhTgco.QXxEjN0wCOzAzNzEzW}
hacker@permissions~changing-file-ownership:~$ ^C
hacker@permissions~changing-file-ownership:~$ 

```
straight fwd
## What I learned
Change owner command (chown)
Root has free access to this command. changes permission of a file to the mentioned user.
syntax: Chown <User> <Filename>
## References 
. 