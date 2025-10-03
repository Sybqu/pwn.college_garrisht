# hidden files :P
find the flag, hidden as a dot-prepended file in /.
**Flag:** pwn.college{sjoB4y9e9gkaCGcwFty_Ik2kApy.QXwUDO0wCOzAzNzEzW}


`

```bash
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.   .dockerenv             bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-200153198323626  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:/$ cat .flag-200153198323626
pwn.college{sjoB4y9e9gkaCGcwFty_Ik2kApy.QXwUDO0wCOzAzNzEzW}
hacker@commands~hidden-files:/$ 
```
reveal hidden files to given
cat the flag
## What I learned
ls -a command to list the hidden files
Ls does not list hidden files by default
## References 
.