# bandit20

### Solution Steps:

1. Save the flag which was obtained from **bandit19**. This flag is actually the password to SSH into **bandit20**.
2. Now establish an SSH connection using `sudo ssh bandit20@bandit.labs.overthewire.org -p 2220`.
3. Here is our clue:
   1. There is a setuid binary in the homedirectory that does the following: 
      1. it makes a connection to localhost on the port you specify as a commandline argument. 
      2. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20)
      3. If the password is correct, it will transmit the password for the next level (bandit21).
4. The concept which needs to understand here is how to send a process in background and then bring back it to foreground.
5. Also another thing which is required to understand here is, working of netcat.
6. Once you understand about netcat, then start a listener on any port, in the background.
7. Execute that binary in the background, which is available in the home directory, by providing the port number on which you have started the netcat listener.
8. Bring the netcat process in foreground and provide the password of current level. After providing the password suspend this process by pressing CTRL+Z.
9. Bring the other process in foreground and you will get a notification like below:
    > Password matches, sending next password
10. Press CTRL+Z and suspend this process.
11. Bring the netcat process in foreground and you will see the password to the next level is printed on the screen :)
12. Save this password and see you in next level :)