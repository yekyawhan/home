---
{"dg-publish":true,"permalink":"/everything-about-linux/kali-fix-ip-address-if-not-obtain-ip/","dgPassFrontmatter":true,"noteIcon":""}
---


	How to fix no ethernet adapter in Kali Linux.
	nano /etc/network/interfaces 
	type the following :
	       auto eth0
	       iface eth0 inet dhcp
	
	nano /etc/resolv.conf
	nameserver 8.8.8.8
	sudo systemctl restart networking.service
	
	------- or -----------
	nano /etc/network/interfaces 
	
	auto eth0
	iface eth0 inet static
	address 192.168.0.100/24
	gateway 192.168.0.1
	
	nano /etc/resolv.conf
	nameserver 8.8.8.8
	sudo systemctl restart networking.service