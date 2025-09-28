# Searching Manuals
Find the option that will give you the flag by reading the challenge man page.
**Flag:** pwn.college{0f9B3Bh0h45hqH2zTUa4TZNvtbq.QX1EDO0wCOzAzNzEzW}




```bash
hacker@man~searching-manuals:~$ man challenge

gzip: stdout: Broken pipe
hacker@man~searching-manuals:~$ --bfjfhe
bash: --bfjfhe: command not found
hacker@man~searching-manuals:~$ /challenge/challenge --bfjfhe
Initializing...
Correct usage! Your flag: pwn.college{0f9B3Bh0h45hqH2zTUa4TZNvtbq.QX1EDO0wCOzAzNzEzW}
hacker@man~searching-manuals:~$ 




```
Searched through it
## What I learned
man command, takes other commands as arguments
The data for commands is stored in a centralized database within our system.
Using the path of the system does not work. Commands as arguments needs to be passed to get the details about the command.
Really helpful use PgUp PgDn to navigate ,h for help and q for quitting the man page.
You can search forwards using "/" and search from the back using "?" use "n" and "N" to go to next search result and previous result
## References 
.