# Matching paths with  []
Starting from your home directory, run /challenge/run with a single argument that bracket-globs into the absolute paths to the file_b, file_a, file_s, and file_h files!


**Flag:**pwn.college{8WeOQxyMj10sW_n4xfdst93eUPJ.QX0IDO0wCOzAzNzEzW}





```bash
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/files_[absh]
Your expansion did not expand to the requested files (/challenge/files/file_b, 
/challenge/files/file_a, /challenge/files/file_s, and /challenge/files/file_h). 
Instead, it expanded to:
/challenge/files/files_[absh]
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[absh]
You got it! Here is your flag!
pwn.college{8WeOQxyMj10sW_n4xfdst93eUPJ.QX0IDO0wCOzAzNzEzW}
hacker@globbing~matching-paths-with-:~$ 

minor typo :P

```
!
## What I learned
File Globbin using single wildcard character "[]" basically repalces [] with any single characters presented within [#characters] ><
If zero files are unmatched the glob remains unchanged  
* the glob matches anypart except or leading "." character
entire paths can be expanded using globbed arguments
## References 
.