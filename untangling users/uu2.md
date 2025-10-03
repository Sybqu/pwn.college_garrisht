# Other users with su  
Launch process in background
**flag**:pwn.college{wMU3oXezRC4beQZFKPky-b5ldfb.QX2UDN1wCOzAzNzEzW}






```bash
hacker@users~other-users-with-su:~$ su zardys
WARNING: you are invoking 'su' without specifying the 'zardus' user.
su: user zardys does not exist
hacker@users~other-users-with-su:~$ su zardus
Password: 
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{wMU3oXezRC4beQZFKPky-b5ldfb.QX2UDN1wCOzAzNzEzW}
zardus@users~other-users-with-su:/home/hacker$ 



```
straightforward :33
## What I learned
su command (substiute user)
It is used to get access to root directory
Older command "from a more civilized time"
Before elevating user privilleges to root , you need to add password to su command.
Modern systems rarely have root passwords and have different mechanismms
su without an argument elevates privilleges to root if authentication is succesful.
An argument can be passed to root , to switch to a particular user instead of root , following the usual password verification process.
## References 
.