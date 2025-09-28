# Helpful Programs
reading a program's documentation with --help
**Flag:**pwn.college{UQAEnJHkIIRtX4DDrI1tnWL52ya.QX3IDO0wCOzAzNzEzW}




```bash
hacker@man~helpful-programs:~$ --help
bash: --help: command not found
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge --fortune
In science it often happens that scientists say, 'You know that's a really
good argument; my position is mistaken,' and then they actually change
their minds and you never hear that old view from them again.  They really
do it.  It doesn't happen as often as it should, because scientists are
human and change is sometimes painful.  But it happens every day.  I cannot
recall the last time something like that happened in politics or religion.
                -- Carl Sagan, 1987 CSICOP keynote address
hacker@man~helpful-programs:~$ /challenge/challenge -g GIVE_THE_FLAG
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]
a challenge to make you ask for help: error: argument -g/--give-the-flag: invalid int value: 'GIVE_THE_FLAG'
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 415
hacker@man~helpful-programs:~$ /challenge/challenge -g 415
Correct usage! Your flag: pwn.college{UQAEnJHkIIRtX4DDrI1tnWL52ya.QX3IDO0wCOzAzNzEzW}
hacker@man~helpful-programs:~$ 




```
read the documentation using --help
## What I learned
Using --help to view docuemntation instead of man
## References 
.