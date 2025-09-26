# Problem 

## Do in Linux

Due to excessive processes held by the nfsuser user. To mitigate this issue, we need to enforce limitations on its maximum processes. Please set the maximum process limits as specified below:

- a. Set the soft limit to 1025


- b. Set the hard limit to 2026

## Solution

`vi /etc/security/limits.config`

```
@nfsuser         soft    nproc           1025
@nfsuser         hard    nproc           2026
```
