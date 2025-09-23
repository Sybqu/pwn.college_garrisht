# Explicit relative paths from /
using "." in relative paths
 ## My solve
**Flag:** pwn.college{outRNK36Jv4CQQIxHJ7LEMaUdqn.QXwUTN0wCOzAzNzEzW}

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for bash.
```bash
hacker@paths~explicit-relative-paths-from-:~$ ./challenge/run
bash: ./challenge/run: No such file or directory
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{outRNK36Jv4CQQIxHJ7LEMaUdqn.QXwUTN0wCOzAzNzEzW}
hacker@paths~explicit-relative-paths-from-:/$ 

```

## What I learned
Explicit relative paths
Using "./" in paths. "." refers to same directory
means challenge is located in the same directory


## References 
.