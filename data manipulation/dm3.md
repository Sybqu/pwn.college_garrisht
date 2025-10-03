# Deleting newlines
Pretty simple! Now you give it a try. I'll intersperse some decoy characters (specifically: ^ and %) among the flag characters. Use tr -d to remove them!
**flag**:pwn.college{ERSalrP30aRa2wbrNaSFEJq44JS.0VNxEzNxwCOzAzNzEzW}



```bash
hacker@data~deleting-newlines:~$ /challenge/run
Your line-split flag: 
p
w
n
.
co
l
l
ege
{ERSalr
P
3
0a
Ra
2w
b
rN
aS
FE
J
q44J
S
.
0V
NxEzN
x
w
COzA
z
N
z
E
z
W
}

hacker@data~deleting-newlines:~$ /challenge/run | tr -d _"\n" 
Your line-split flag: pwn.college{ERSalrP30aRa2wbrNaSFEJq44JS.0VNxEzNxwCOzAzNzEzW}hacker@data~deleting-newlines:~$ /challenge/run | tr -d  "\n" 
Your line-split flag: pwn.college{ERSalrP30aRa2wbrNaSFEJq44JS.0VNxEzNxwCOzAzNzEzW}hacker@data~deleting-newlines:~$ ^C
hacker@data~deleting-newlines:~$ 
```
straightforward :33
## What I learned
tr command : translate
It translates the character provided in its first argument to character provided in its second argument. It can also handle multiple characters, with the characters in different positions of the first argument replaced with assosciated characters in the second argument.
"-d" flag in tr command.
tr -d can be used to delete characters in the output.
Newlines can be deleted or translated .
tr -d _"\n"
here backslash (\) signifies that character that follows is a standin.
## References 
.