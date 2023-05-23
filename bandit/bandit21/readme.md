# bandit21

### Solution Steps:

1. Save the flag which was obtained from **bandit20**. This flag is actually the password to SSH into **bandit21**.
2. Now establish an SSH connection using `sudo ssh bandit21@bandit.labs.overthewire.org -p 2220`.
3. Find the clues below:
   1. A program is running automatically at regular intervals from cron, the time-based job scheduler.
   2. Look in /etc/cron.d/ for the configuration and see what command is being executed.
4. This level is straight forward. You just need to see the related cronjob in /etc/cron.d directory.
5. Once you will see the contents you will easily understand which bash file you have to check.
6. Once you will read that shell script, you will understand to how to get the password for the next level :)
7. Along the way, understand what cronjob really is. In its simplest form, cronjob in linux is like scheduled task in windows. Commands or mentioned in crontab are meant to be executed at specific time.
8. You can further read about it [here](https://en.wikipedia.org/wiki/Cron)
9. Save the password and see you in next level :)