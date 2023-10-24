---
{"dg-publish":true,"permalink":"/everything-about-linux/network-respring-or-restart-network-device/","dgPassFrontmatter":true,"noteIcon":""}
---

	service network-manager restart (ဒီဟာနဲ့တင်ရတယ်)
	ip မရခဲ့ရင်ဝင်ပြင်ရမယ်
	nano /etc/network/interfaces
	static ကိုပြောင်းမယ် dhcp
	ip ရေးထားတဲ့ ပထမ ၂ကြောင်းကိုဖျက်မယ်
	systemctl restart networking.service
	ရပြီ
