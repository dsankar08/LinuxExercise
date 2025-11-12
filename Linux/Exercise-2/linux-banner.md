# Problem 

## Do in Linux

- Update the message of the day on all application and db servers for Nautilus. Make use of the approved template located at /home/thor/nautilus_banner on jump host

## Solution

- `scp -r /<file> tony@stapp01:home/tony`
- copy the file to all the app and db servers
- login into all the app and db servers
- check for banner file
- move the file to /etc/motd
- `sudo mv <banner-file> /etc/motd`
- `cat /etc/motd`
- `exit`
- login again to check
