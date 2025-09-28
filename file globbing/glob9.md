# Multiple options for Tab completion
This challenge has a /challenge/files directory with a bunch of files starting with pwncollege. Tab-complete from /challenge/files/p or so, and make your way to the flag!

**Flag:**pwn.college{w8rQ807USlAEgkA-recTcIV-zXQ.0lN0EzNxwCOzAzNzEzW}






```bash
hacker@globbing~multiple-options-for-tab-completion:~$ cd /challenge/files
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat pwncollege-
pwncollege-family      pwncollege-flag        pwncollege-flamingo    pwncollege-flyswatter  pwncollege-hacking     
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat pwncollege-
pwncollege-family      pwncollege-flag        pwncollege-flamingo    pwncollege-flyswatter  pwncollege-hacking     
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat pwncollege-f
pwncollege-family      pwncollege-flag        pwncollege-flamingo    pwncollege-flyswatter  
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat pwncollege-fl
pwncollege-flag        pwncollege-flamingo    pwncollege-flyswatter  
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat pwncollege-fla
pwncollege-flag      pwncollege-flamingo  
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat pwncollege-flag 
pwn.college{w8rQ807USlAEgkA-recTcIV-zXQ.0lN0EzNxwCOzAzNzEzW}
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ 


```
Ts easy chat
## What I learned
tab spam~~~~~~~
auto completion
using * can lead to unintentional errors.
Bash will auto-expand until the first point where multiple options spawn. When tab is pressed during this scenario, the plausible options are listed below , other shells may cycle instead of priting plausible options


## References 
.