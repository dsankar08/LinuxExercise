# Problem 

## Do in Linux

- a. Your task is to disable direct SSH root login on all app servers within the Stratos Datacenter.

## Solution

 `vi /etc/ssh/sshd_config`
 Change `permitrootlogin` to no
 restart sshd service
 `systemctl restart sshd`
