# Problem 

## Do in Linux

- install the required packages of SElinux on App server 2 in Stratos Datacenter and disable it permanently for now; it will be enabled after making some required configuration changes on this host. Don't worry about rebooting the server as there is already a reboot scheduled for tonight's maintenance window. Also ignore the status of SElinux command line right now; the final status after reboot should be disabled.

## Solution

`yum -y install selinux*  `

```
vi /etc/selinux/config 

SELINUX=disabled

```
