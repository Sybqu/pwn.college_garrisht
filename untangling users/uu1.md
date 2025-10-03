# Becoming Root with su     
Gain access to root using su command
**flag**:pwn.college{snWGaU_Rn7naW2lH0aAaPL_94ai.QX1UDN1wCOzAzNzEzW}





```bash
hacker@users~becoming-root-with-su:~$ su
Password: 
root@users~becoming-root-with-su:/home/hacker# ls /
bin  boot  challenge  dev  etc  flag  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
root@users~becoming-root-with-su:/home/hacker# cd /
root@users~becoming-root-with-su:/# 
root@users~becoming-root-with-su:/# ls
bin  boot  challenge  dev  etc  flag  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
root@users~becoming-root-with-su:/# cat flag
pwn.college{snWGaU_Rn7naW2lH0aAaPL_94ai.QX1UDN1wCOzAzNzEzW}
root@users~becoming-root-with-su:/# ^C
root@users~becoming-root-with-su:/# 

```
straightforward :33
## What I learned
su command (substiute user)
It is used to get access to root directory
Older command "from a more civilized time"
Before elevating user privilleges to root , you need to add password to su command.
Modern systems rarely have root passwords and have different mechanismms
## References 
.