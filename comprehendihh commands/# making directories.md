# making directories
make directory and file in given location
**Flag:**pwn.college{swTZk6-Uq2q72kidJDMmVzvcwaq.QXxMDO0wCOzAzNzEzW}



```bash
hacker@commands~making-directories:~$ mkdir /temp/pwn
mkdir: cannot create directory ‘/temp/pwn’: No such file or directory
hacker@commands~making-directories:~$ cd /
hacker@commands~making-directories:/$ ls
bin  boot  challenge  dev  etc  flag  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@commands~making-directories:/$ mkdir /tmp/pwn/dihh
mkdir: cannot create directory ‘/tmp/pwn/dihh’: No such file or directory
hacker@commands~making-directories:/$ mkdir temp
mkdir: cannot create directory ‘temp’: Permission denied
hacker@commands~making-directories:/$ mkdir tmp
mkdir: cannot create directory ‘tmp’: File exists
hacker@commands~making-directories:/$ cd /tmp/pwn
bash: cd: /tmp/pwn: No such file or directory
hacker@commands~making-directories:/$ cd /tmp
hacker@commands~making-directories:/tmp$ ls
bin  hsperfdata_root  tmp.TpSOPGOVKK
hacker@commands~making-directories:/tmp$ mkdir pwn
hacker@commands~making-directories:/tmp$ cd pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ cd college
bash: cd: college: Not a directory
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{swTZk6-Uq2q72kidJDMmVzvcwaq.QXxMDO0wCOzAzNzEzW}
hacker@commands~making-directories:/tmp/pwn$ ^C
hacker@commands~making-directories:/tmp/pwn$ 

```
i tried making directory directly but didnt work out,
made a few typos and them boom
## What I learned
mkdir command to make directories
i wonder why the absolute path didnt work
## References 
.