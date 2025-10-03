# Translating Characters
 /challenge/run will print the flag but will swap the casing of all characters (e.g., A will become a and vice-versa). Can you undo it with tr and get the flag?
**flag**:pwn.college{w8Oa3Dr5FKjhjmKmC3W9QUrhRBz.01MxEzNxwCOzAzNzEzW}




```bash
hacker@data~translating-characters:~$ /challenge/run
Your case-swapped flag:
PWN.COLLEGE{W8oA3dR5fkJHJMkMc3w9quRHrbZ.01mXeZnXWcoZaZnZeZw}

hacker@data~translating-characters:~$ /challenge/run | tr ABCDEFGHIJKLMNOPQRSTUVQXYZ abcdefghijklmnopqrstuvwxyz
your case-swapped flag:
pWn.college{W8oa3dr5fkjhjmkmc3w9qurhrbz.01mxeznxWcozaznzezw}

hacker@data~translating-characters:~$ /challenge/run | tr ABCDEFGHIJKLMNOPQRSTUVWXYZ abcdefghijklmnopqrstuvwxyz
your case-swapped flag:
pwn.college{w8oa3dr5fkjhjmkmc3w9qurhrbz.01mxeznxwcozaznzezw}

hacker@data~translating-characters:~$ ^C
hacker@data~translating-characters:~$ ^C
hacker@data~translating-characters:~$ /challenge/run | tr ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ
yOUR CASE-SWAPPED FLAG:
pwn.college{w8Oa3Dr5FKjhjmKmC3W9QUrhRBz.01MxEzNxwCOzAzNzEzW}

hacker@data~translating-characters:~$ ^C
hacker@data~translating-characters:~$ ^C
hacker@data~translating-characters:~$ 

```
I ended up switching all uppercase to lowercase to first so yeah only half toggling
Then i tried it altogether. I looked for a way to shorten this tho and we can use "-" to  cover the range of the alphabets
## What I learned
tr command : translate
It translates the character provided in its first argument to character provided in its second argument. It can also handle multiple characters, with the characters in different positions of the first argument replaced with assosciated characters in the second argument.
## References 
.