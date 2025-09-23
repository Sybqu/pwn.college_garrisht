# Implicit relative paths from /
run /challenge/run using a relative path while having a current working directory of /.
## My solve
**Flag:** pwn.college{oxwAVWlwGCj3bDmjJSz3OxWxO_t.QX5QTN0wCOzAzNzEzW}

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for bash.
```bash
hacker@paths~implicit-relative-paths-from-:~$ challenge/run
bash: challenge/run: No such file or directory
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{oxwAVWlwGCj3bDmjJSz3OxWxO_t.QX5QTN0wCOzAzNzEzW}
hacker@paths~implicit-relative-paths-from-:/$ 
```
Switched to the root directory Then used a relative path to invoke the command
as challenge is located in inside root
## What I learned
Relative paths start from current working directory.
Relative paths do not start at the root 
Cwd is where the prompt is currently located at
If it does not start with "/" or "~" its a relative path
## References 
.