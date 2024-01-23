---
{"dg-publish":true,"permalink":"/everything-about-linux/disk-expand-kali-linux/","dgPassFrontmatter":true,"noteIcon":""}
---

	
	method 1 fdisk -l
	method 2 df -H
	
	apt-get install gparted  
	linuxswap  ကို swap off right click
	cylinder ကိုရွေးပေးရမယ်

```
Resize partition: `sudo cfdisk`

Extend PV physical volume: `pvresize /dev/sda3`

Extend logical volume: `lvextend -l +100%FREE /dev/ubuntu-vg/ubuntu-lv`

Resize: `resize2fs /dev/mapper/ubuntu--vg-ubuntu--lv`
```

or 

```
sudo su -
fdisk -l
growpart /dev/sda 3
pvresize /dev/sda3
lvextend -l +100%FREE /dev/ubuntu-vg/ubuntu-lv
resize2fs  /dev/mapper/ubuntu--vg-ubuntu--lv
df -h
```