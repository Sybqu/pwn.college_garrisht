# comparing files
use diff to find difference and find the flag
**Flag:** ` pwn.college{ErE5fu3LCc6Vgp3QzVCFto8dayl.01MwMDOxwCOzAzNzEzW}
`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for bash.
```bash
hacker@commands~comparing-files:~$ cd/challenge
bash: cd/challenge: No such file or directory
hacker@commands~comparing-files:~$ cd /challenge
hacker@commands~comparing-files:/challenge$ diff decoys_only.txt decoys_and_real.txt
85a86
> pwn.college{ErE5fu3LCc6Vgp3QzVCFto8dayl.01MwMDOxwCOzAzNzEzW}
hacker@commands~comparing-files:/challenge$ ^C
hacker@commands~comparing-files:/challenge$ 
```
navigated to directory then ran the command
## What I learned
Diff command
it compares to different files line by line and shows us whats exactly the difference
It is more efficient than plain eyeballing
"<>" are used to specify the files in the output
it uses "a c d"
add change delete respectively
the numbers around them are used to denote the line numbers
## References 
.