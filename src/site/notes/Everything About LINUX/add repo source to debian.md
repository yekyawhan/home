---
{"dg-publish":true,"permalink":"/everything-about-linux/add-repo-source-to-debian/","dgPassFrontmatter":true,"noteIcon":""}
---


	nano /etc/apt/sources.list  
  
and paste this into it  
  
deb [http://http.kali.org/kali](http://http.kali.org/kali) kali main non-free contrib  
  
  
deb [http://security.kali.org/kali-security](http://security.kali.org/kali-security) kali/updates main contrib non-free  
  
  
deb-src [http://http.kali.org/kali](http://http.kali.org/kali) kali main non-free contrib  
  
  
deb-src [http://security.kali.org/kali-security](http://security.kali.org/kali-security) kali/updates main contrib non-free  
  
save it  
  
then now update  
  
apt-get update && apt-get install -y linux-headers-$(uname -r)  
  
after smooth completion  
  
use  
  
sudo reboot now  
  
to ensure all packages and new services restart their functions