# Problem 

## Do in Linux

- a. Install cups package on all the application servers.

- b. Once installed, make sure it is enabled to start during boot.

## Solution

- login to all the app servers
- `sudo yum -y install cups`
- `sudo systemctl enable cups`
- check the service status `sudo systemctl status cups`
