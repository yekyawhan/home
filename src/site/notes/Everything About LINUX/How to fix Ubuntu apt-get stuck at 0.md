---
{"dg-publish":true,"permalink":"/everything-about-linux/how-to-fix-ubuntu-apt-get-stuck-at-0/","dgPassFrontmatter":true,"noteIcon":""}
---

	When I do upgrade, it gets stuck here
user@plato:~# apt-get update 0% [Connecting to us.archive.ubuntu.com (2001:67c:1562::14)] [Connecting to sec░

	how to get apt-get to work again.

Edit [`gai.conf`](http://manpages.ubuntu.com/gai.conf.5):

```
nano /etc/gai.conf
```

change line ~54 to uncomment the following:

```
precedence ::ffff:0:0/96  100
```

write and quit:

```
:wq
```

**Solution 1:**

Try using  `https`  repository by executing the following command
```
echo "deb https://http.kali.org/kali kali-rolling main non-free contrib" > /etc/apt/sources.list
```
Then try  `sudo apt-get update`  If you find the same error, please choose another solution.

**Solution 2:** please execute the following command.

apt-key adv --keyserver hkp://keys.gnupg.net --recv-keys 7D8D0BF6

Then try  `sudo apt-get update`  If you find the same error, please choose another solution.

**Solution 3:** Please keep a back up file before changing the sources.list file Using text editor add these lines to  `/etc/apt/sources.list`  file

```
deb http://http.kali.org/ /kali main contrib non-free
deb http://http.kali.org/ /wheezy main contrib non-free
deb http://http.kali.org/kali kali-dev main contrib non-free
deb http://http.kali.org/kali kali-dev main/debian-installer
deb-src http://http.kali.org/kali kali-dev main contrib non-free
deb http://http.kali.org/kali kali main contrib non-free
deb http://http.kali.org/kali kali main/debian-installer
deb-src http://http.kali.org/kali kali main contrib non-free
deb http://security.kali.org/kali-security kali/updates main contrib non-free
deb-src http://security.kali.org/kali-security kali/updates main contrib non-free 
```
Then try  `sudo apt-get update`  If you find the same error, please choose another solution.

**solution 4:** Are you using any proxy server? Then,

check the file  `/etc/apt/apt.conf`

Please add the following three lines in  `/etc/apt/apt.conf`

Acquire::http::proxy "http://proxy:port/"; 
Acquire::ftp::proxy "ftp://proxy:port/"; 
Acquire::https::proxy "https://proxy:port/";

write your IP address in place of 'proxy'

write your port number in place of 'port'

Then try  `sudo apt-get update`  If you find the same error, please choose another solution.