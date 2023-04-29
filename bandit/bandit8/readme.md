# bandit8

### Solution Steps:

1. Save the flag which was obtained from **bandit7**. This flag is actually the password to SSH into **bandit8**.
2. Now establish an SSH connection using `sudo ssh bandit8@bandit.labs.overthewire.org -p 2220`.
3. Following are the clues which are given to us:
   * Password for the next level is stored in a file named **data.txt**.
   * The line which contains password is the only unique line
4. We can use following command to have an idea of data which we are dealing with:
   > `wc -l < filename`
5. It turned out that there are a total of 1001 lines available in this file. Out of these lines, only one is of our interest.
6. The rule here is to first `sort` the file and then pipe the result to `uniq` command to find the desired line.
   > `cat filename | uniq -u`
7. Voila! you have found your flag. Save it somewhere and use it to login to next level.
8. Thank you for your time. See you in next level :)  
   <p align=center><img src=bandit8-flag.png alt=""></p>