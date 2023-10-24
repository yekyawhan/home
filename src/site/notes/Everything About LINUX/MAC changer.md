---
{"dg-publish":true,"permalink":"/everything-about-linux/mac-changer/","dgPassFrontmatter":true,"noteIcon":""}
---


	ifconfig
	ifconfig eth0 | grep ether
	
	macchanger --help
	macchanger -s eth0  (showing manufacture)

	crontab --help
	sudo crontab -e

add this line

	@reboot macchanger -r eth0  (reboot ချတဲ့အချိန်မှာပဲ run မယ်)
	
	  
