# Deleting Characters
Pretty simple! Now you give it a try. I'll intersperse some decoy characters (specifically: ^ and %) among the flag characters. Use tr -d to remove them!
**flag**:pwn.college{I6ySFdsZaUZtJp_Qfbr3ZQ8AQHo.0FNxEzNxwCOzAzNzEzW}



```bash
hacker@data~deleting-characters:~$ cat flag
cat: flag: No such file or directory
hacker@data~deleting-characters:~$ /challenge/run
Your character-stuffed flag:
p%w^n.%c^%ol%l^%e^%g^%e^%{^%I6%y%S^F^%d^s%Z^a^%U^%Z^%tJp_Q^f%b%r^3^Z%Q%8^%A^%Q^Ho^%.0^%F^Nx^E^%z^%N^%x%w^C%O^%zA^%z%N%z^%E^%z^%W^%}^%^%
hacker@data~deleting-characters:~$ /challenge/run | tr -d ^%
Your character-stuffed flag:
pwn.college{I6ySFdsZaUZtJp_Qfbr3ZQ8AQHo.0FNxEzNxwCOzAzNzEzW}
hacker@data~deleting-characters:~$ ^C
hacker@data~deleting-characters:~$ 
```
straightforward :33
## What I learned
tr command : translate
It translates the character provided in its first argument to character provided in its second argument. It can also handle multiple characters, with the characters in different positions of the first argument replaced with assosciated characters in the second argument.
"-d" flag in tr command.
tr -d can be used to delete characters in the output.
## References 
.