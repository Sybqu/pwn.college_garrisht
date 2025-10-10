# Groups and files
n this level, I have made the flag readable by whatever group owns it, but this group is currently root.
 Luckily, I have also made it possible for you to invoke chgrp as the hacker user! Change the group ownership of the flag file,
  and read the flag!
  **Flag:**pwn.college{QIkRi852CFk2zju9KaiAAL3IeX_.QXxcjM1wCOzAzNzEzW}
`

```bash
hacker@permissions~groups-and-files:~$ id
uid=1000(hacker) gid=1000(hacker) groups=1000(hacker)
hacker@permissions~groups-and-files:~$ ls -l
total 36
-rw-r--r-- 1 hacker hacker  27 Sep 30 14:42 1
-rw-r--r-- 1 hacker hacker   4 Sep 28 13:28 COLLEGE
drwxr-xr-x 1 hacker hacker   0 Sep 23 04:18 Desktop
-rw-r--r-- 1 hacker hacker   8 Sep 28 13:57 PWN
-rw-r--r-- 1 root   hacker  60 Sep 23 18:33 a
drwxr-xr-x 1 hacker hacker  20 Sep 30 17:21 ae
-rw-r--r-- 1 root   hacker  60 Sep 23 08:06 f
-rw-r--r-- 1 hacker hacker   0 Sep 30 14:59 flag_fifo
-rw-r--r-- 1 hacker hacker 829 Sep 28 13:45 instructions
-rw-r--r-- 1 hacker hacker  95 Sep 28 13:45 myflag
drwxr-xr-x 1 hacker hacker  26 Sep 30 17:25 not-the-flag
drwxr-xr-x 1 hacker hacker   0 Sep 28 09:41 not-the0flag
-rw-r--r-- 1 hacker hacker  77 Sep 30 14:02 pwn
-rw-r--r-- 1 hacker hacker 437 Sep 28 13:39 the-flag
hacker@permissions~groups-and-files:~$ chgrp hacker /flag
hacker@permissions~groups-and-files:~$ cat flag
cat: flag: No such file or directory
hacker@permissions~groups-and-files:~$ cat /flag
pwn.college{QIkRi852CFk2zju9KaiAAL3IeX_.QXxcjM1wCOzAzNzEzW}
hacker@permissions~groups-and-files:~$ 

```
straight fwd
## What I learned
Sharing is built into Linux Design.
Files have owning user and a group.
groups can have a multiple users and users can exist in groups.

id command can be used to check which groups we are a part of.
Helps access differnet resources from different users   
group ownership can be changed using chgrp
## References 
. 