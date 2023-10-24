---
{"dg-publish":true,"permalink":"/everything-about-linux/essential-command-line-setup-linux-guide/","dgPassFrontmatter":true,"noteIcon":""}
---

```
sudo apt clean && sudo apt update && sudo apt full-upgrade -y && sudo apt autoremove -y && sudo apt autoclean -y && sudo snap refresh
```
```
apt-get nano cmatrix python3-pip neofetch htop fuzz smbmap tilix netdiscover npm nodejs xrdp remmina timeshift ranger trash piper libreoffice snap
```
```forsnap
sudo apt install snapd
sudo snap install core
```
```
sudo snap install telegram-desktop
```
	(backup system )
	timeshift "backup whole system "
	
	set  #variable ကိုကြည့်တာ
	this commennt must be home diretory
	cat .zsh
	nano .zshrc
	smbclient -U yekyawhan //192.168.0.196/video
	
	lsb_release -a
	apt install pwn
	apt install enum4linux
	
	smbmap -H 192.168.0.108
	
	python 2 — python -m SimpleHTTPServer 8000
	Python3 —m http.server 8080

* remote desktop for kali*
```
sudo apt install xrdp
```
```
systemctl enable xrdp
```
```
systemctl start xrdp
```
```
systemctl status xrdp
```

	After XRDP is installed you can start the services with the following command:

	service xrdp-sesman start
	update-rc.d xrdp enable     
	service xrdp status
	Now you should be able to RDP directly into your Kali Linux:
	
	ip address fix by manully
	=================
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
	
	***AlmaLinux**
	1. Use the following command to restart the server networking service.
    

    # nmcli networking off
    # nmcli networking on
    or

```
systemctl restart NetworkManager
```

	office 
	====
	apt isntall libreoffice
	
	sublime
	=====
	download from official site deb file
	sudo dpkg -i filename.deb
	
	if you don't want download use this repo
	wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/sublimehq-archive.gpg > /dev/null
	
	
	undercover mode (like windows)
	===========
	kali-undercover
	
	
	this mode for power saving & performance mode
	===============================
	don't use vm machine is not working
	apt install cpufrequtils
	use this command 
	sudo cpufreq -set -g powersave
	sudo cpufreq-set -g performance
	
	
	why linux battery usage more
	=====================
	1-you can reduce battery life time
	=======================
	apt install tlp
	apt search tlp
	add-apt-repository ppa:linuxuprising/apps
	apt install tlp-ui
	
	2-u can try second way 
	===============
	apt install powertop