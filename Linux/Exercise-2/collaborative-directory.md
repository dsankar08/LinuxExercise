# Problem 

## Do in Linux

- Setup a collaborative directory /sysops/data on app server 3 in Stratos Datacenter.

- The directory should be group owned by the group sysops and the group should own the files inside the directory. The directory should be read/write/execute to the user and group owners, and others should not have any access.

## Solution

- `mkdir -p /sysops/data`
- `ls -l sysops`
- `getfacl sysops/data`
- `chgrp -R sysops sysops` (change group owner) / chown sysops:sysops /sysops [owner:group  /folder]
- `chmod -R 2770 sysops/data` (change permission of file 2 is a )
- check `getfacl sysops/data`


When you set the setgid bit (2) on a directory, it changes how files and subdirectories created inside it inherit group ownership:

Without setgid (770):

New files/folders take the primary group of the user who created them.

With setgid (2770):

New files/folders inherit the group of the parent directory, not the user’s group.
