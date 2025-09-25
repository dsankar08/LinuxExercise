# Problem 

## Do in Linux

- Adjust the default runlevel on all App servers in Stratos Datacenter to enable GUI booting by default. It's imperative not to initiate a server reboot after completing this task.

## Solution

- Login to all servers and run `systemctl set-default graphical.target`

  graphical.target - for GUI
  multi-user.target - CLI
