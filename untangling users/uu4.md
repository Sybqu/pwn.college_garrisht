# using Sudo 
In this level, we will give you sudo access, and you will use it to read the flag. Nice and easy!
**flag**:pwn.college{ECTeEMEnNV31z4Y0Hlz9yjAa4-t.QX4UDN1wCOzAzNzEzW}


```bash
hacker@users~using-sudo:~$ sudo ls
1  COLLEGE  Desktop  PWN  a  ae  f  flag_fifo  instructions  myflag  not-the-flag  not-the0flag  pwn  the-flag
hacker@users~using-sudo:~$ sudo cd /
sudo: cd: command not found
hacker@users~using-sudo:~$ cd /
hacker@users~using-sudo:/$ ls
bin  boot  challenge  dev  etc  flag  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@users~using-sudo:/$ sudo cat flag
pwn.college{ECTeEMEnNV31z4Y0Hlz9yjAa4-t.QX4UDN1wCOzAzNzEzW}
hacker@users~using-sudo:/$ 

```
BRO MY STUPID AHH DOWNLOADED JOHN THE RIPPER AND THEN I WAS ONTO SUMN TUTORIAL ON HOW TO USE IT BRO HOLY SHIT I WASTED SO MUCH TIME 
i understand it now.
## What I learned
sudo command (superuser do (originally))
 now , (substitute user , do)
 unlike su which asks for password first, sudo defaults to running a command as root
 Anyhow , apparently root passwords are hard to maintain and they can leak (hashes) in larger environments
 sudo checks **policies** to determine user authorization . These policies are defined in an externally directory /etc/sudoers
## References 
.