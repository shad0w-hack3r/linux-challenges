# bandit13

### Solution Steps:

1. Save the flag which was obtained from **bandit12**. This flag is actually the password to SSH into **bandit13**.
2. Now establish an SSH connection using `sudo ssh bandit13@bandit.labs.overthewire.org -p 2220`.
3. Following are the clues which are given to us:
   * Password for the next level is stored in a file named **/etc/bandit_pass/bandit14** and can only be read by user bandit14.
   * You get a private SSH key that can be used to log into the next level.
4. Once you are logged in to **bandit13**, in the home directory you will find a private SSH key. We will use this SSH key to login to **bandit14**. 
5. Why we are doing this? Because **bandit13** cannot access our clue file which is available in **/etc/bandit_pass** directory.
6. We will connect with **bandit14** using following command:
   > `ssh bandit14@hostname -p 2220 -i key_filename`
7. Once login is successful, simply just **cat** the file which is mentioned in our clue.
8. Voila! Flag found :) Save it for next level.
