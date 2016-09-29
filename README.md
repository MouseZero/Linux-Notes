# Static IP
-----
Figure out what your network device is called via "ifconfig". The following example assumes your device name is "enp0s9"

edit /etc/network/interfaces

```
auto enp0s9
iface enp0s9 inet static
address 192.168.0.75
gateway 192.168.0.1
netmask 255.255.255.0
network 192.168.0.0
broadcast 192.168.0.255
dns-nameservers 8.8.8.8 8.8.4.4
```
