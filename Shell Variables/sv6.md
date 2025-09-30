# Storing command output 
Read the output of the /challenge/run command directly into a variable called PWN, and it will contain the flag!


**Flag:**FLAG=pwn.college{0My98HNKF0ocv-XcWAVYLuvrobk.QX1cDN1wCOzAzNzEzW}




```bash
hacker@variables~storing-command-output:~$ PWN=$(cat /challenge/run)
hacker@variables~storing-command-output:~$ echo $PWN
#!/opt/pwn.college/bash if [ -t 1 ] || [ ! -f /tmp/subshell ] then fold -s >&2 <<< "You are not running me via Command Substitution! Please make sure to run me with command substitution." exit 1 elif [ ! -f /tmp/dstvar ] then fold -s >&2 <<< 'You do not appear to be reading into a variable... Make sure to read me into a variable, e.g.:' echo ' VAR_NAME=$(/challenge/run)' >&2 exit 2 fi [ -f /tmp/dstvar ] && read DSTVAR < /tmp/dstvar if [ "$DSTVAR" != "PWN" ] then fold -s >&2 <<< "You are reading into the $DSTVAR variable, but you should read into the PWN variable. I am redacting the flag!" echo "pwn.college{REDACTED}" exit 3 fi fold -s >&2 <<< "Congratulations! You have read the flag into the PWN variable. Now print it out and submit it!" cat /flag
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out 
and submit it!
hacker@variables~storing-command-output:~$ cat $PWN
cat: pwn.college{0My98HNKF0ocv-XcWAVYLuvrobk.QX1cDN1wCOzAzNzEzW}: No such file or directory
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{0My98HNKF0ocv-XcWAVYLuvrobk.QX1cDN1wCOzAzNzEzW}
hacker@variables~storing-command-output:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~storing-command-output
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=ac67bdff9946a19cbb7f14603db8a38be6165a246458cd453313be3e18e790d5
HOME=/home/hacker
LANG=C.UTF-8
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env
hacker@variables~storing-command-output:~$ export PWN
hacker@variables~storing-command-output:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~storing-command-output
PWN=pwn.college{0My98HNKF0ocv-XcWAVYLuvrobk.QX1cDN1wCOzAzNzEzW}
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=ac67bdff9946a19cbb7f14603db8a38be6165a246458cd453313be3e18e790d5
HOME=/home/hacker
LANG=C.UTF-8
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env
hacker@variables~storing-command-output:~$ 




```
Easy enough just messing around

## What I learned
Command substitution. It is used to store the output of commands in a variable . 
Sytax : $() or `` . 
Pwncollege ganggang prefers $()
## References 
.