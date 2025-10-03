# finding files
make directory and file in given location
**Flag:**pwn.college{E3GIucqbP2Yd8-2VCQ0e_TubFhE.QX1ITO0wCOzAzNzEzW}




```bash
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /challenge/DESCRIPTION.md
Correct argument! Here is the /challenge/DESCRIPTION.md file:
While using most commands is straightforward, the usage of some commands can get quite complex.
For example, the arguments to commands like `sed` and `awk`, which we're definitely not getting into right now, are entire programs in an esoteric programming language!
Somewhere on the spectrum between `cd` and `awk` are commands that take arguments to their arguments...

This sounds crazy, but you've already encountered this with the `find` level in [Basic Commands](/linux-luminarium/commands).
`find` has a `-name` argument, and the `-name` argument itself takes an argument specifying the name to search for.
Many other commands are analogous.

Here is this level's documentation for `/challenge/challenge`:

> Welcome to the documentation for `/challenge/challenge`! This program allows you to print arbitrary files to the terminal, when given the `--printfile` argument. The argument to the `--printfile` argument is the path of the flag to read. For example, `/challenge/challenge --printfile /challenge/DESCRIPTION.md` will print out the description of the level!

Given that documentation, go get the flag!
hacker@man~learning-complex-usage:~$ --printfile flag
bash: --printfile: command not found
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{E3GIucqbP2Yd8-2VCQ0e_TubFhE.QX1ITO0wCOzAzNzEzW}
hacker@man~learning-complex-usage:~$ ......... .. . . . .  . ..  . . . . .. . . . . . . .


```
--printfile instead of cat worked
## What I learned
importance of correct arguments and absolute paths while using the documentation
## References 
.