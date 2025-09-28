# Mixing globs
We put a few happy, but diversely-named files in /challenge/files. Go cd there and run /challenge/run, providing a single argument: a short (3 characters or less) globbed word with two * globs in it that covers every word that contains the letter p.


**Flag:**pwn.college{YVTOds5QHyq4mP1wBElnMhP7iS0.0lM3kjNxwCOzAzNzEzW}






```bash
hacker@globbing~mixing-globs:~$ /challenge/files
bash: /challenge/files: Is a directory
hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run *i[on]*
Error: your argument is too long! It must be 6 characters or less.
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run *[on]*
Your expansion did not expand to the requested files (challenging, educational, 
pwning). Instead, it expanded to:
amazing challenging educational fantastic incredible jovial kind laughing nice optimistic pwning queenly radiant splendid thrilling uplifting victorious wonderful xenial youthful
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run *[ng]*
Your expansion did not expand to the requested files (challenging, educational, 
pwning). Instead, it expanded to:
amazing challenging delightful educational fantastic great incredible kind laughing magical nice pwning queenly radiant splendid thrilling uplifting wonderful xenial
hacker@globbing~mixing-globs:/challenge/files$ *[lw]*
bash: beautiful: command not found
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run *[lw]*
Your expansion did not expand to the requested files (challenging, educational, 
pwning). Instead, it expanded to:
beautiful challenging delightful educational incredible jovial laughing magical pwning queenly splendid thrilling uplifting wonderful xenial youthful
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cpe]*
You got it! Here is your flag!
pwn.college{oDEtPyjhTS6ai-FyQV1evO42-C7.QX1IDO0wCOzAzNzEzW}
hacker@globbing~mixing-globs:/challenge/files$ 


```
confusing ahh ahh ahh
## What I learned
Multiple globbing ><
Bash supports the expansion of multiple globs in a single word

## References 
.