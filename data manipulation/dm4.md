# Extracting the first lines with head
This challenge's /challenge/pwn outputs a bunch of data, and you'll need to pipe it through head to grab just the first 7 lines and then pipe them onwards to /challenge/college,
**flag**:pwn.college{Mgc5X54opsyUPjCK1F-WFvewyoI.0lNxEzNxwCOzAzNzEzW}




```bash
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/run | head -n 7 | /challenge/college
bash: /challenge/run: No such file or directory
Invalid codes!
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -n 7 | /challenge/college
Congratulations, you piped the right codes!
pwn.college{Mgc5X54opsyUPjCK1F-WFvewyoI.0lNxEzNxwCOzAzNzEzW}
hacker@data~extracting-the-first-lines-with-head:~$ ^C
hacker@data~extracting-the-first-lines-with-head:~$ 
```
straightforward :33
## What I learned
head command. The head command is used to display the first few lines of its input.
By default it shows first 10 lines but it can be controlled using -n option
head -n <no.of.lines.of.output>
## References 
.