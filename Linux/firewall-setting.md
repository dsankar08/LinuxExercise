# Problem 

## Do in Linux

- Allow all incoming connections on port 8087/tcp. Ensure the zone is set to public.

## Solution

`sudo firewall-cmd --zone=public --list-all`

```
public
  target: default
  icmp-block-inversion: no
  interfaces: 
  sources: 
  services: dhcpv6-client ssh
  ports: 
  protocols: 
  masquerade: no
  forward-ports: 
  source-ports: 
  icmp-blocks: 
  rich rules:
```

`sudo firewall-cmd --zone=public --permanent --add-port=5001/tcp`

`firewall-cmd --reload`

```
sudo firewall-cmd --zone=public --list-all


public
  target: default
  icmp-block-inversion: no
  interfaces: 
  sources: 
  services: dhcpv6-client ssh
  ports: 5001/tcp
  protocols: 
  masquerade: no
  forward-ports: 
  source-ports: 
  icmp-blocks: 
  rich rules:
```
