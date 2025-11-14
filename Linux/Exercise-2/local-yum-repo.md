# Problem 

## Do in Linux

- a. We have some packages already present at location /packages/downloaded_rpms/ on Nautilus Backup Server.


- b. Create a yum repo named yum_local and make sure to set Repository ID to yum_local. Configure it to use package's location /packages/downloaded_rpms/.


- c. Install package samba from this newly created repo.

## Solution

-  login to backup server
- configure the new repo
- `cd /etc/yum.repos.d/`
- `sudo vi yum_local.repo`
```
[yum_local]
name=yum_local
baseurl=file:///packages/downloaded_rpms/
gpgcheck=0
enabled=1

```
- `yum clean all`
- `yum update`
- `yum repolist`
- `sudo yum install -y --enablerepo="yum_local" samba`
- enable and start the service
