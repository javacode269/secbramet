# Linux
### INSTALL CENTOS
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
      gateway4: 192.168.157.2
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
Lưu ý: khi dùng máy ảo mode NAT network adapter
  => Cần check default gateway để điều chỉnh cho đúng
```

### QUYEN TRUY CAP TRONG LINUX
1. Tao user trong linux
```
# adduser
# useradd 
# usermod -aG devops2 manhnv1
# chmod g=rwx ./data (Co 3 option ugo dai dien cho user, group, other)

----
Khi nao user thi se tao mot group tuong ung vs user do
```
### TU DUY TRIEN KHAI DU AN
1. Tư duy triển khai hệ thống

```
1. Công cụ là gì
2. File cấu hình ở đâu
3. Làm sao để build
4. Run như thế nào?
```

2. Tư duy bảo vệ hệ thống
 
```
1. Thư mục làm việc riêng
2. User cho dự án riêng
```