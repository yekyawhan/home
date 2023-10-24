---
{"dg-publish":true,"permalink":"/everything-about-linux/vmware-share-folder-in-kali-linux/","dgPassFrontmatter":true,"noteIcon":""}
---

 ```
vmware-hgfsclient
```
	apt install vmware-hgfsclient 
	sudo nano /etc/fstab

	If you do not have a section reserved to shared folders, please add this instructions at the end of the file.

```
# Use shared folders between VMWare guest and host  
.host:/Raid0-3TB /home/y3kh/mnt/raid0 fuse.vmhgfs-fuse defaults,allow_other,uid>
```


This is on terminal

```shell
sudo vmware-hgfsclient .host:/Raid0-3TB    /home/y3kh/mnt/raid0 fuse.vmhgfs-fuse defaults,allow_other,uid=1000 0 0
```

```
sudo vmware-hgfsclient .host:/Raid0-3TB ~/mnt/raid0 -o allow_other -o uid=1000
```
