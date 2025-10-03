# grepping for a needle in a haystack
finding flag using grep
**Flag:** `pwn.college{8fEiwuTvwyEMdAccA-_V2rW0sIn.QX3EDO0wCOzAzNzEzW}
`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for bash.
```bash
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{8fEiwuTvwyEMdAccA-_V2rW0sIn.QX3EDO0wCOzAzNzEzW}
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ 

```
Grep command
flags begin with "pwn.college"
entered the argument got the result
if i entered cat it displayed all the files inside. hence grep grapples it.
## What I learned
Grep command
Sometimes the files that need to be "cat"'d are too big. hence grep is a more efficient way to search
Syntax: grep SEARCH_STRING /path/to/file

## References 
.