---
{"tags":["cifs-nfs"],"dg-publish":true,"permalink":"/everything-about-linux/mount-nfs-and-cifs/","dgPassFrontmatter":true,"noteIcon":""}
---


`apt install nfs-kernel-server (for server if not don't use)`
`sudo apt install nfs-common (client only connect)`
`sudo apt install cifs-utils`
`nfs method (temporary method) This will be in terminal`
```
sudo mount -t nfs 192.168.0.196:/volume1/video/Ebook /ebook
```
```
sudo mount -t cifs -o username=yekyawhan //192.168.0.196/video /video
```

	sudo mount -t cifs -o username=yekyawhan //192.168.0.196/usbshare1 /home/y3kh/mnt/test-ykh

### temporaty method
```
sudo mount -t nfs 100.105.111.121:volume1/Bloggerandsoftware /home/y3kh/mnt/test-ykh
```
```
sudo mount -t nfs 192.168.0.196:/volume1/Bloggerandsoftware /home/y3kh/mnt/software
```
```
100.105.111.121:volume1/music /music nfs
```
### nfs method (permanent)

```
sudo mount -t cifs //server/share /mnt/mountpoint -o username=your_username,password=your_password
```
	nano /etc/fstab
	192.168.0.196:volume1/video /home/y3kh/mnt/video nfs
	192.168.0.196:/volume1/Bloggerandsoftware/obsidian-sync-y3kh /home/y3kh/mnt/obsidian-sync-y3kh nfs

### cifs method (working no pass)

sudo nano /etc/fstab
\\192.168.0.6\d /home/y3kh/mnt/ykh-desktop cifs

### cifs setup on kali-linux (is working y3kh)

	mkdir video
	mkdir obsidian-sync-y3kh
	create password file on 
	sudo chmod 777 video
	/home/y3kh/mnt/.pass
	username=yekywhan
	password=password

```shell
//192.168.0.196/Bloggerandsoftware/obsidian-sync-y3kh           /home/y3kh/mnt/obsidian-sync-y3kh cifs credentials=/home/y3kh/mnt/.pass,iocharset=utf8,gid=1000,uid=1000,file_mode=0777,dir_mode=0777 0 0
```
	sudo mount -a
	df -h
### nfs folder mount on windows system

	mount -o -u:yekyawhan \\192.168.0.196\volume1\video t:

this method for anon method ok by y3kh

	mount -o anon \\192.168.0.196\volume1\video\ i:

### This working on my Kali-laptop

```shell
192.168.0.196:volume1/video /mnt/video nfs  
//192.168.0.196/music /mnt/music cifs credentials=/home/y3kh/mnt/.pass,iocharset=utf8,gid=1000,uid=1000,file_mode=0777,dir_mode=0777 0 0  
//192.168.0.196/video/Ebook /home/y3kh/mnt/ebook cifs credentials=/home/y3kh/mnt/.pass,iocharset=utf8,gid=1000,uid=1000,file_mode=0777,dir_mode=0777 0 0
```

```
192.168.0.196:volume1/nextcloud /mnt/nextcloud nfs
192.168.0.196:volume1/music /mnt/music nfs
192.168.0.196:volume1/Ebook /mnt/ebook nfs
```
