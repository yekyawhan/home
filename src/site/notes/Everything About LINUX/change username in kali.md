---
{"dg-publish":true,"permalink":"/everything-about-linux/change-username-in-kali/","dgPassFrontmatter":true,"noteIcon":""}
---


	sudo -i
	passwd root
	pkill -u yekyawhan

try to log in root and passwd gui

	 usermod –l y3kh –d /home/yekyawhan –m yekyawhan
	 groupmod -n y3kh yekyawhan
	sudo ln -s /home/y3kh /home/yekyawhan
	sudo chfn -f "y3kh-kali" y3kh

cat /etc/passwd
cat /etc/group
reboot
