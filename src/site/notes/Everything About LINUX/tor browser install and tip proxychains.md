---
{"dg-publish":true,"permalink":"/everything-about-linux/tor-browser-install-and-tip-proxychains/","dgPassFrontmatter":true,"noteIcon":""}
---

	sudo apt install tor -y
	sudo systemctl status tor
	service tor status
	service tor start
	sudo systemctl enable tor
	service tor restart  (afterusing of stuck)
	sudo nano /etc/proxychains4.conf
	dynamic ok
	
	(change: socket 5  127.0.0.1  9050)
	  (socket4 125.26.99.228 44052)
	you can use any app start using with proxychains 
		eg:firefox :nmap:
	proxychains firefox www.duckduckgo.com
--------------------



	proxy-list on github 
	https://github.com/TheSpeedX/PROXY-List
	copy >> socket4 >> address list>> 
	and check here
	https://hidemyna.me/en/proxy-checker



	i use this proxy
	
	172.67.181.97:80         |United States|
	104.27.50.151:80         217ms
	190.93.244.178:80          24ms
	103.21.244.145:80         24ms
	172.67.182.40
	 167.86.99.172
	
