---
{"dg-publish":true,"permalink":"/everything-about-linux/linux-network-address/","dgPassFrontmatter":true,"noteIcon":""}
---

	
	echo "nameserver 8.8.8.8" | sudo tee /etc/resolv.conf > /dev/null
	
	echo "nameserver 8.8.8.8" | sudo tee /etc/resolvconf/resolv.conf.d/base > /dev/null
	
	echo "nameserver 208.67.222.222" | sudo tee /etc/resolvconf/resolv.conf.d/base > /dev/null
		
	sudo nano /etc/apt/sources.list
		
	Temporary resolve
	It is likely that this issue is either:
	
	temporary due to your Internet Service Provider not correctly forwarding internet naming (DNS) to either its or external DNS servers, or
	due to a change in your network has similarly blocked this naming - for example, new router/modem, reconfiguring a switch with a new configuration.
	Lets look at the possible DNS resolving issues.
	
	First, temporarily add a known DNS server to your system.
	
	echo "nameserver 8.8.8.8" | sudo tee /etc/resolv.conf > /dev/null
	Then run sudo apt-get update.
	
	If this fixes your temporary resolving messages then either wait for 24 hours to see if your ISP fixes the issue for you (or just contact your ISP) - or you can permanently add a DNS server to your system:
	
	echo "nameserver 8.8.8.8" | sudo tee /etc/resolvconf/resolv.conf.d/base > /dev/null
	8.8.8.8 is Google's own DNS server.
	
	source
	
	Another example DNS server you could use is OpenDNS - for example:
	
	echo "nameserver 208.67.222.222" | sudo tee /etc/resolvconf/resolv.conf.d/base > /dev/null
	package-management issues
	In addition to the temporary resolve issues - you have a few package management issues that need to be corrected - I'm assuming you have tried recently to upgrade from one Ubuntu version to the next recommended version - in your case from Natty (11.04) to Oneiric (11.10)
	
	Open a terminal and type
	
	sudo nano /etc/apt/sources.list
	Look for lines that have your a different distribution name in the list than you were expecting - in your case - you have upgraded to oneiric but you have another release name natty
	
	For example, look for lines that look like deb http:/archive.canonical.com/ natty backports
	
	Add a # to the beginning of the line to comment it out - for example
	
	#deb http:/archive.canonical.com/ natty backports
	
	Save and re-run:
	
	sudo apt-get update && sudo apt-get upgrade