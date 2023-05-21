# bandit18

### Solution Steps:

1. Save the flag which was obtained from **bandit17**. This flag is actually the password to SSH into **bandit18**.
2. Now establish an SSH connection using `sudo ssh bandit18@bandit.labs.overthewire.org -p 2220`.
3. Wait what? Once you enter the correct password, and you login successfully, you will immediately get log out from the machine. Why? Below is the clue:
   1. The password for the next level is stored in a file readme in the homedirectory.
   2. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.
4. To overcome this issue, we need to find a way to provide ssh password, in the same command, while logging into this machine. To achieve this task I used **sshpass** utility. This utility allows us to submit SSH password in one liner. Following is the command:
   > `sshpass -p password ssh bandit18@bandit.labs.overthewire.org -p 2220`
5. Another clue we have is the location of **readme** file. This file is available in the home directory of current user (ofcourse). So to read that file we have to provide them command in same one line e.g. like below:
   > `sshpass -p password ssh bandit18@bandit.labs.overthewire.org -p 2220 cat pathToFile`
6. Once you will figure out the correct path, just use the above command and you will easily get the flag for next level :)
7. Save this password as it will be used to login to next level :)