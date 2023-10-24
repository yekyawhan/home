---
{"dg-publish":true,"permalink":"/everything-about-linux/get-terminal-pro/","dgPassFrontmatter":true,"noteIcon":""}
---

	python3 -c 'import pty; pty.spawn("/bin/bash")'
	export PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/tmp
	export TERM=xterm-256color
	alias ll='ls -lsaht --color=auto'
	Ctrl + Z [Background Process]
	stty raw -echo ; fg ; reset
	stty columns 200 rows 200

