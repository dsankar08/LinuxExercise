# Problem 

## Do in Linux

- Configure crontab access on App Server 2 as follows: Allow crontab access to mariyam user while denying access to the jerome user.

## Solution

- Create two files in `/etc/cron.allow` and `/etc/cron.deny`
- add users there depending on request
