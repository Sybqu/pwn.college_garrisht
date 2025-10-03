# Other users with su  
crack password
**flag**:pwn.college{gPtsvPRBpMhigC3isBJMttri9sZ.QX3UDN1wCOzAzNzEzW}






```bash
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
0g 0:00:00:02 28% 1/3 0g/s 259.4p/s 259.4c/s 259.4C/s sudraz!..bzardus
0g 0:00:00:07 74% 1/3 0g/s 267.0p/s 267.0c/s 267.0C/s 9999961..z9999945
aardvark         (zardus)
1g 0:00:00:21 100% 2/3 0.04591g/s 267.3p/s 267.3c/s 267.3C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak --show
hacker:NO PASSWORD:20357:0:99999:7:::
zardus:aardvark:20364:0:99999:7:::

2 password hashes cracked, 0 left
hacker@users~cracking-passwords:~$ su zardus
Password: 
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{gPtsvPRBpMhigC3isBJMttri9sZ.QX3UDN1wCOzAzNzEzW}
zardus@users~cracking-passwords:/home/hacker$ 

```
BRO MY STUPID AHH DOWNLOADED JOHN THE RIPPER AND THEN I WAS ONTO SUMN TUTORIAL ON HOW TO USE IT BRO HOLY SHIT I WASTED SO MUCH TIME 
i understand it now.
## What I learned
su command (substiute user)
It is used to get access to root directory
Older command "from a more civilized time"
Before elevating user privilleges to root , you need to add password to su command.
Modern systems rarely have root passwords and have different mechanismms
su without an argument elevates privilleges to root if authentication is succesful.
An argument can be passed to root , to switch to a particular user instead of root , following the usual password verification process.
Cracking password via hash leak
So in short if you have a hash password can be cracked
hash : one way encryption of password
even tho password reading permissions is only available to the root password leaks happen frequently
## References 
.