# Changing Permissions
In this challenge, you must change the permissions of the /flag file to read it! Typically, you need to have write access to the file in order to change its permissions, but I have made the chmod command all-powerful for this level, and you can chmod anything you want even though you are the hacker user. This is an ultimate power. The /flag file is owned by root, and you can't change that, but you can make it readable. Go and solve this
  **Flag:**pwn.college{YmLqllGY8xdGuJXAiAbZ0yQrNqp.QXzcjM1wCOzAzNzEzW}


`

```bash
hacker@permissions~changing-permissions:~$ chmod a+rw /flag
hacker@permissions~changing-permissions:~$ cat /flag
pwn.college{YmLqllGY8xdGuJXAiAbZ0yQrNqp.QXzcjM1wCOzAzNzEzW}
hacker@permissions~changing-permissions:~$ 

```
straight fwd c
## What I learned
First character of a file denotes the file type
The next 9 character shows permission
3 for permissions of owning user
3 for permissions of owning group
3 for permissions of other access
~ r - user/group/other can read the file (or list the directory)
w - user/group/other can modify the files (or create/delete files in the directory)
x - user/group/other can execute the file as a program (or can enter the directory, e.g., using `cd`)
- - nothing ~
File permission can be changed using chmod (change mode) command
syntax: chmod [OPTIONS] MODE FILE
Mode can be specified in 2 ways: modification of existing mode or a completely new mode
chmod allows you to tweak permissions with the mode format of WHO+/-WHAT, where WHO is user/group/other and WHAT is read/write/execute.
## References 
. 