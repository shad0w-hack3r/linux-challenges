# bandit22

### Solution Steps:

1. Save the flag which was obtained from **bandit21**. This flag is actually the password to SSH into **bandit22**.
2. Now establish an SSH connection using `sudo ssh bandit22@bandit.labs.overthewire.org -p 2220`.
3. Find the clues below:
   1. You need to understand a shell script which you will find by looking in /etc/cron.d/ directory.
4. Along the way you will learn about a md5 hash. Just for the sake of understanding, hashing algorithm produces a fixed length output to whatever input size given to it. A slight modification in input will totally change the output hash value.
5. Also please note that, hash function has to be non-reversible. It means that, one should not be able to reconstuct the input from its hash value.
6. After understanding the script, you have to look for a file in /tmp directory. There is a small catch here, you have to find the exact name of the file and then use `cat` command to read its contents. 
7. That file in /tmp directory contains the password to the next level :)
8. Save this password and see you in next level :)