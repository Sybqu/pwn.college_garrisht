# Printed exported variables
Try the env command: it'll print out every exported variable set in your shell, and you can look through that output to find the FLAG variable!
**Flag:**FLAG=pwn.college{0kdwnDhP1AKEEo6Wh4h9Q8Rr2vp.QX4UTN0wCOzAzNzEzW}






```bash
hacker@variables~printing-exported-variables:~$ man env
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=850964edf78d421113b0389276bf50fc11e6c4641991ea64c519f8e2e90473e7
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{0kdwnDhP1AKEEo6Wh4h9Q8Rr2vp.QX4UTN0wCOzAzNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env
hacker@variables~printing-exported-variables:~$ ^C
hacker@variables~printing-exported-variables:~$ 



```
used man env to get to know more about it . Apparently its supposed to run a program in a modfied environment
## What I learned
Learning the env command which without any arguments prints all exported variables in our shell
## References 
.