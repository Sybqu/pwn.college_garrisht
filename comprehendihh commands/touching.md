# Touching files :P
Touch the files ^^
**Flag:** `pwn.college{E1X6WSF4Vbnm8od0y9QG5ozFgJh.QXwMDO0wCOzAzNzEzW}

`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for bash.
```bash
hacker@commands~touching-files:~$ touch /temp/pwn
touch: cannot touch '/temp/pwn': No such file or directory
hacker@commands~touching-files:~$ cd /temp
bash: cd: /temp: No such file or directory
hacker@commands~touching-files:~$ cd /
hacker@commands~touching-files:/$ cd temp
bash: cd: temp: No such file or directory
hacker@commands~touching-files:/$ ls
bin  boot  challenge  dev  etc  flag  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@commands~touching-files:/$ touch /tmp/pwn
hacker@commands~touching-files:/$ touch /tmp/college
hacker@commands~touching-files:/$ /challenge/run
Success! Here is your flag:
pwn.college{E1X6WSF4Vbnm8od0y9QG5ozFgJh.QXwMDO0wCOzAzNzEzW}
```
Touched the files via an absolute path
## What I learned
Touching >:-)
## References 
.