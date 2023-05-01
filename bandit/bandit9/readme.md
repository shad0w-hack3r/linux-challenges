# bandit9

### Solution Steps:

1. Save the flag which was obtained from **bandit8**. This flag is actually the password to SSH into **bandit9**.
2. Now establish an SSH connection using `sudo ssh bandit9@bandit.labs.overthewire.org -p 2220`.
   
   !["bandit9-ssh"](bandit9-ssh.png)

3. Following are the clues which are given to us:
   * Password for the next level is stored in a file named **data.txt**.
   * Line starts with multiple **=** signs



