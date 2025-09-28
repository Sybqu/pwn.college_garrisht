# Matching with  []
Starting from your home directory, change your directory to /challenge, but use the ? character instead of c and l in the Change your working directory to /challenge/files and run /challenge/run with a single argument that bracket-globs into file_b, file_a, file_s, and file_h!



**Flag:**pwn.college{cBd23LXeIMvAKXsE2i-lvNPtoi0.QXzIDO0wCOzAzNzEzW}




```bash
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ ls
file_a  file_c  file_e  file_g  file_i  file_k  file_m  file_o  file_q  file_s  file_u  file_w  file_y
file_b  file_d  file_f  file_h  file_j  file_l  file_n  file_p  file_r  file_t  file_v  file_x  file_z
hacker@globbing~matching-with-:/challenge/files$ /challenge/run
Error: you did not use a square bracket glob...
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[absh]
You got it! Here is your flag!
pwn.college{cBd23LXeIMvAKXsE2i-lvNPtoi0.QXzIDO0wCOzAzNzEzW}
hacker@globbing~matching-with-:/challenge/files$ 




```
!
## What I learned
File Globbin using single wildcard character "[]" basically repalces [] with any single characters presented within [#characters] ><
If zero files are unmatched the glob remains unchanged  
* the glob matches anypart except or leading "." character
## References 
.