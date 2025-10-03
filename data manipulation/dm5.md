# Extracting specific sections of head
The -d argument specifies the column delimiter (how columns are separated). In this case, it's a space character. Of course, it has to be in quotes here so that the shell knows that the space is an argument rather than a space separating other arguments! The -f argument specifies the field number (which column to extract).

In this challenge, the /challenge/run program will give you a bunch of lines with random numbers and single characters (characters of the flag) as columns. Use cut to extract the flag characters, then pipe them to tr -d "\n" (like the previous level!) to join them together into a single line.
**flag**:pwn.college{I_UJC99MAk5tNpFSmHRRlijJRaK.01NxEzNxwCOzAzNzEzW}




```bash
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d " " -f 2 | tr -d "\n"
pwn.college{I_UJC99MAk5tNpFSmHRRlijJRaK.01NxEzNxwCOzAzNzEzW}hacker@data~extracting-specific-sections-of-text:~$ ^C
hacker@data~extracting-specific-sections-of-text:~$ 

```
straightforward :33
## What I learned
cut command.
used to extract specific data from columns.
syntax : cut -d " " -f <column no>
here " " space is in quotes so that the shell knows that the space is an argument rather than a space separating other arguments
## References 
.