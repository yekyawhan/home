---
{"dg-publish":true,"permalink":"/everything-about-linux/switching-desktop-environments/","dgPassFrontmatter":true,"noteIcon":""}
---

	
```
sudo apt update
```
```
tasksel --list-tasks
```
​တစ်ခုကိုသွင်းပါ kali-desktop-core: Any key tools required for a GUI image 
```
sudo apt install -y kali-desktop-core
```
```
sudo apt install -y kali-desktop-e17
```
```
sudo apt install -y kali-desktop-gnome
```
```
sudo apt install -y kali-desktop-i3
```
```
sudo apt install -y  kali-desktop-kde
```
or
```
sudo apt install kde-full
```
```
sudo apt install -y kali-desktop-lxde
```
```
sudo apt install -y kali-desktop-mate
```
```
sudo apt install -y kali-desktop-xfce
```
```
sudo update-alternatives --config x-session-manager
```

ပြန်ဖြုတ်တာ

```
sudo apt purge --autoremove kali-desktop-xfce
```
