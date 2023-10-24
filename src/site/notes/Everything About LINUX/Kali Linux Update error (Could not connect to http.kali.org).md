---
{"dg-publish":true,"permalink":"/everything-about-linux/kali-linux-update-error-could-not-connect-to-http-kali-org/","dgPassFrontmatter":true,"noteIcon":""}
---

	
	
	nano /etc/apt/source.list
	(change to first line to )
	deb http://kali.download/kali kali-rolling main contrib non-free non-free-firmware
	
	or
	
	$ kali-tweaks
	change to https 

https://www.youtube.com/watch?v=9n0u3IbGT0M&t=113s