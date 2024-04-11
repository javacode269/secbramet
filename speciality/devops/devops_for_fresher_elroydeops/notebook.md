# Linux
### install centos
1. Cau hinh card mang co dinh

File /etc/netplan/00-installer-config.yaml default
``` 
# This is the network config written by 'subiquity'
network:
  ethernets:
    ens33:
      dhcp4: true
  version: 2
```
Change to ====>
``` 
/etc/netplan/00-installer-config.yaml
# This is the network config written by 'subiquity'
network:
  ethernets:
    ens33:
      dhcp4: false
      addresses: [192.168.157.128/24]
      addresses: 192.168.1.1
  version: 2
```


```
tiennnv65 comment
--------
file cau hinh duoc viet duoi dang cau truc yaml
ens: Ethernet Network Switch
wlan: wireless local area network
convention khi dat ten cua card mang:
tiep sau cac loai card mang nhu ens/wlan la cac ky hieu chu va so
Numeric identifier: 33 y chi la card mang ethernet thu 33 cua trong may
additional characters: 
```
1. 