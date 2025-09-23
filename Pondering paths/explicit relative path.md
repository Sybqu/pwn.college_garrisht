# implicit relative path
using explicity relative paths to run command
## My solve
**Flag:** `pwn.college{09A4rxNba0kFOxqTbk2j7Dm9_jw.QXxUTN0wCOzAzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for bash.
```bash
hacker@paths~implicit-relative-path:~$ ./run
bash: ./run: No such file or directory
hacker@paths~implicit-relative-path:~$ cd /
hacker@paths~implicit-relative-path:/$ cd challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{09A4rxNba0kFOxqTbk2j7Dm9_jw.QXxUTN0wCOzAzNzEzW}
hacker@paths~implicit-relative-path:/challenge$ 


```

## What I learned
linux explicity avoids looking in current directory when we provide a naked path.this is a safety measure
as we could accidentaly run commands in our current directory. hence they lead to error
## References 
