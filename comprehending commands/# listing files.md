# listing files
list the files in given directory to find the flag
**Flag:** `pwn.college{sYPJaL2XANcf6Eka0_9nIYcC_Zp.QX4IDO0wCOzAzNzEzW}

`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for bash.
```bash
hacker@commands~listing-files:~$ ls /challenge
21905-renamed-run-12368  DESCRIPTION.md
hacker@commands~listing-files:~$ cat 21905-renamed-run-12368
cat: 21905-renamed-run-12368: No such file or directory
hacker@commands~listing-files:~$ cd /challenge
hacker@commands~listing-files:/challenge$ cat 21905-renamed-run-12368
#!/opt/pwn.college/bash

echo "Yahaha, you found me! Here is your flag:"
cat /flag
hacker@commands~listing-files:/challenge$ cd ^C
hacker@commands~listing-files:/challenge$ /21905-renamed-run-12368
bash: /21905-renamed-run-12368: No such file or directory
hacker@commands~listing-files:/challenge$ ./21905-renamed-run-12368
Yahaha, you found me! Here is your flag:
pwn.college{sYPJaL2XANcf6Eka0_9nIYcC_Zp.QX4IDO0wCOzAzNzEzW}
hacker@commands~listing-files:/challenge$ ^C
hacker@commands~listing-files:/challenge$ ^C
hacker@commands~listing-files:/challenge$ 
```
Apparently i catenated the file content and wasted time thinking i was troll but im dumb as hell. Forgot to run the file ffs.
## What I learned
Ls command..
interaction.
navigation
## References 
.