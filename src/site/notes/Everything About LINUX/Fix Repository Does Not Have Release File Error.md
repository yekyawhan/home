---
{"dg-publish":true,"permalink":"/everything-about-linux/fix-repository-does-not-have-release-file-error/","dgPassFrontmatter":true,"noteIcon":""}
---


	[

## Switching Kali Main Branch

	check this
	grep -v '#' /etc/apt/sources.list | sort -u

	echo "deb http://http.kali.org/kali kali-rolling main contrib non-free non-free-firmware" | sudo tee /etc/apt/sources.list

	echo "deb http://http.kali.org/kali kali-last-snapshot main contrib non-free non-free-firmware" | sudo tee /etc/apt/sources.list
	
	sudo apt update
	kali-tweaks


	[

## Enabling Kali Additional Branches

	kali-experimental
	echo "deb http://http.kali.org/kali kali-experimental main contrib non-free non-free-firmware" | sudo tee /etc/apt/sources.list.d/kali-experimental.list

	sudo rm /etc/apt/sources.list.d/kali-experimental.list
	echo "deb http://http.kali.org/kali kali-bleeding-edge main contrib non-free non-free-firmware" | sudo tee /etc/apt/sources.list.d/kali-bleeding-edge.list
	sudo rm /etc/apt/sources.list.d/kali-bleeding-edge.list
	