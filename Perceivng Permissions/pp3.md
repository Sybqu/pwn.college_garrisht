# Fun with Group and Names
You will need to use the id command to figure that name out, then chgrp to victory!
  **Flag:**pwn.college{kZAT67hBLbkHhf3wUyveoQpw6wN.QXycjM1wCOzAzNzEzW}

`

```bash
hacker@permissions~fun-with-groups-names:~$ id
uid=1000(hacker) gid=1000(grp371) groups=1000(grp371)
hacker@permissions~fun-with-groups-names:~$ chgrp grp371 /flag
hacker@permissions~fun-with-groups-names:~$ cat /flag
pwn.college{kZAT67hBLbkHhf3wUyveoQpw6wN.QXycjM1wCOzAzNzEzW}
hacker@permissions~fun-with-groups-names:~$ 

```
straight fwd c
## What I learned
Sharing is built into Linux Design.
Files have owning user and a group.
groups can have a multiple users and users can exist in groups.

id command can be used to check which groups we are a part of.
Helps access differnet resources from different users   
group ownership can be changed using chgrp
## References 
. 