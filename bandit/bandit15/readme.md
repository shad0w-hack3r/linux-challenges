# bandit15

### Solution Steps:

1. Save the flag which was obtained from **bandit14**. This flag is actually the password to SSH into **bandit15**.
2. Now establish an SSH connection using `sudo ssh bandit15@bandit.labs.overthewire.org -p 2220`.
3. Here is our clue:
   1. The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption.
4. 