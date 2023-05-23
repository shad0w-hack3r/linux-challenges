# bandit19

### Solution Steps:

1. Save the flag which was obtained from **bandit18**. This flag is actually the password to SSH into **bandit19**.
2. Now establish an SSH connection using `sudo ssh bandit19@bandit.labs.overthewire.org -p 2220`.
3. Here is our clue:
   1. A setuid binary is present in home directory.
   2. Execute it without arguments to find out how to use it.
   3. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.
4. 