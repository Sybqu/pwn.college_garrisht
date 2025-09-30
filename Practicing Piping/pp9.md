# Filtering with grep -v
Use grep -v to filter out all the lines containing "DECOY" and reveal the real flag!
**Flag:**pwn.college{cD1mfD8iRCGqH71-f_JD_8A2VIh.0FOxEzNxwCOzAzNzEzW}



```bash
hacker@piping~filtering-with-grep-v:~$ ^C
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{cD1mfD8iRCGqH71-f_JD_8A2VIh.0FOxEzNxwCOzAzNzEzW}
hacker@piping~filtering-with-grep-v:~$ ^C
hacker@piping~filtering-with-grep-v:~$ 


```
Followed the instructions straight up, not much trouble, Didnot need to redirect anything.
## What I learned
Filtering with grep -v(invert match). Normal grep shows lines that match a pattern where as grep -v shows lines that do NOT match a pattern :3. Seems fair as looking for data u dont want to filter the data u need is a really method.
## References 
.