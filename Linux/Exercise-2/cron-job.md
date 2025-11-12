# Problem 

## Do in Linux

- a. Install cronie package on all Nautilus app servers and start crond service.

- b. Add a cron */5 * * * * echo hello > /tmp/cron_text for root user.

## Solution

- `sudo yum -y install cronie*`
- `systemctl start crond`
- `systemctl status crond`
- `sudo crontab -e`
- add the cron job
- restart the crond
- check `sudo crontab -l -u root`
- check `sudo cat /var/spool/cron/root`
