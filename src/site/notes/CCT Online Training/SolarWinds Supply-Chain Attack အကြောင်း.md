---
{"tags":["malware"],"dg-publish":true,"permalink":"/cct-online-training/solar-winds-supply-chain-attack/","dgPassFrontmatter":true,"noteIcon":""}
---


### solar winds အကြောင်းပြောရမယ်ဆိုရင် ဆိုလာဝင်းဆို တာ orinion platform ပေါ်မှာ run တဲ့ survillian တမျိုးပဲ
It Technician စနစ်စီမံခန့်ခွဲမှုကိရိယာများတွင် အဓိကအားဖြင့် ပေးဆောင်သည့် ဆော့ဖ်ဝဲကုမ္ပဏီတစ်ခုဖြစ်သည်။ အကျယ်ပြန့်ဆုံးအသုံးချနိုင်သော SolarWinds ထုတ်ကုန်မှာ ကွန်ရက်စီမံခန့်ခွဲမှုစနစ် (NMS) ဖြစ်သည့် Orion ဖြစ်သည်။ 
**ကွန်ရက်လုံခြုံရေး စောင့်ကြည့်နေသည့် NSM နှင့် မမှားစေလိုပါ။**
#### Orion Platform ထုတ်ကုန်များ

```ad-tldr
title: ကွန်ရက်စွမ်းဆောင်ရည်စောင့်ကြည့်
NETFLOW လမ်းကြောင်းဆိုင်ရာ ခွဲခြမ်းစိတ်ဖြာသူ
ကွန်ရက်ဖွဲ့စည်းမှုမန်နေဂျာ
IP လိပ်စာမန်နေဂျာ
VOIP နှင့် ကွန်ရက်အရည်အသွေး မန်နေဂျာ
အသုံးပြုသူ စက်ပစ္စည်း ခြေရာခံသူ
ဆာဗာနှင့် အပလီကေးရှင်း မော်နီတာ
ဆာဗာပြင်ဆင်မှု မော်နီတာ
သိုလှောင်မှုအရင်းအမြစ်စောင့်ကြည့်
VIRTUALIZATION မန်နေဂျာ
ဝဘ်စွမ်းဆောင်ရည်စောင့်ကြည့်
မှတ်တမ်းခွဲခြမ်းစိတ်ဖြာသူ
node တွေကို ၁၀၀ ကနေ ၁၀၀၀ ထိကို handle လုပ်နိုင်တယ်

```
solar wind ရဲ့ case နောက်ကွယ် က rusia  ပူတင်က လုပ်တာလို့လည်းထင်ကြတယ် ဒါကို ပူတင်တို့ဘက်က ညင်းထားတယ်

![Orion Platform.png|undefined](/img/user/Images%20All/cct-images/Orion%20Platform.png)


```ad-abstract
title: ခံခဲ့ရပုံ
2020 ဇွန်လအစောပိုင်းမှာ SolarWinds ဆော့ဖ်ဝဲလ်တွင် အားနည်းချက်တစ်ခုကို အသုံးချခြင်းဖြင့် တရားရေးဌာန ဆာဗာကို တိုက်ရိုက် ဖောက်ဖျက်ခဲ့ကြောင်း စုံစမ်းစစ်ဆေးသူများက သံသယရှိကြတယ်
SolarWinds ဆော့ဖ်ဝဲလ်ကို အမှန်ပင် ဖောက်ထွင်းဝင်ရောက်ခဲ့သည်။ စုံစမ်းစစ်ဆေးသူများသည် ယခင်က မမြင်ဖူးသော နည်းပညာများကို အသုံးပြု၍ ဟက်ကာများသည် ကုမ္ပဏီ၏ ဖောက်သည် ထောင်ပေါင်းများစွာထံ ဝင်ရောက်ခွင့်ရရှိခဲ့သည်။ ကူးစက်ခံရသူများထဲတွင် အမေရိကန်ကာကွယ်ရေးဌာန၊ အမိမြေလုံခြုံရေးဌာနနှင့် ဘဏ္ဍာရေးဌာနတို့အပါအဝင် ဖက်ဒရယ်အေဂျင်စီ ရှစ်ခုထက်မနည်းပါဝင်သော်လည်း Intel၊ Cisco နှင့် Palo Alto Networks အပါအဝင် ထိပ်တန်းနည်းပညာ နှင့် လုံခြုံရေး ကုမ္ပဏီများ — သူတို့သိသေးတာ။ Microsoft နှင့် Mandiant တို့ပင် ခံရသူများစာရင်းတွင် ပါဝင်ခဲ့သည်။

```

```ad-bug
title: ဝင်ရောက်ပုံဝင်ရောက်နည်း
• It is known that the malware was deployed as
an update from SolarWinds' own servers and
was digitally signed by a valid digital
certificate bearing their name
• This strongly points to a supply chain attack
• The certificate was issued by Symantec
• Serial Number:
0fe973752022a606adf2a36e345dc0ed
**Supply Chain ကနေဝင်လာတာပေါ့နော်**
```

18,000 of its 300,000 Orion customers are impacted


```ad-todo
title: သဲလွန်စ
နိုဝင်ဘာလ ၁၀ ရက်နေ့၊2020
multifactor authentication စနစ်တွင် ဖုန်းအသစ်ကို ဝန်ထမ်းတစ်ဦးမှ စာရင်းသွင်
ဆက်စပ်နေသည့် ဖုန်းနံပါတ်မရှိ စက်ပစ္စည်းများသို့ တစ်ကြိမ်ဝင်ရောက်ခွင့်ကုဒ်များ ပေးပို့ခဲ့သည်
**Samsung phone had been used to log in from the Florida IP address at the same time the employee**
attackers set up a dedicated **command-and-control** server* and gave that machine a name that partly mimicked the name a real system on the victim’s network might have

```
```
လူကြိုက်အများဆုံး ထုတ်ကုန်များထဲမှ တစ်ခုဖြစ်သော Orion ဟုခေါ်သော ဆော့ဖ်ဝဲအစုံကို အသုံးပြုနေပါသည်။
ဆော့ဖ်ဝဲလ်သည် ရံဖန်ရံခါ အပ်ဒိတ်များကို ရယူရန်အတွက်သာ SolarWinds ကွန်ရက်နှင့် ဆက်သွယ်နေသင့်သည်။
ယင်းအစား ၎င်းသည် ဟက်ကာများ၏ အမိန့်ပေးချက်နှင့် ထိန်းချုပ်ရေးဆာဗာဖြစ်ဖွယ်ရှိသည့် အမည်မသိစနစ်တစ်ခုကို ဆက်သွယ်နေခြင်းဖြစ်သည်။
```

Willi Ballenthin နှင့် အခြားနှစ်ဦးကို ရှာဖွေရန် တာဝန်ပေးအပ်ခဲ့ဖိုင်ပေါင်း 18,000 ကျော်နှင့် ကုဒ်နှင့် ဒေတာ 14 ဂစ်ဂါဘိုက် ပါဝင်
24 hours အတွင်းမှာ ဖိုင်လေးတစ်ဖိုင်ကိုတွေ့ခဲ့တယ် အဲ့နေ့ကတော့ 'ဒီဇင်ဘာ၁၁ ရက်နေ့'

FireEye သည် နိုင်ငံတစ်နိုင်ငံမှ ဟက်ခ်ခံရကြောင် ဒီဇင်ဘာလ 8 ရက်နေ့မှာစတင် ကြေညာခဲ့တယ်


![Pasted image 20231119004622.png|300](/img/user/Images%20All/cct-images/Pasted%20image%2020231119004622.png)
Fire Eye CEO Mandiant, Kevin Mandia
![Pasted image 20231119145712.png|undefined](/img/user/Images%20All/cct-images/Pasted%20image%2020231119145712.png)
![Pasted image 20231119143502.png|undefined](/img/user/Images%20All/cct-images/Pasted%20image%2020231119143502.png)
	indicator of compromise (ioc)
![Pasted image 20231119144442.png|undefined](/img/user/Images%20All/cct-images/Pasted%20image%2020231119144442.png)


<iframe width="560" height="315" src="https://www.youtube.com/embed/Kf7Motm36Go?si=IJCJ3Wb2TVsFRMG1" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>




အနှစ်ချုုပ် conclusion
if goverment 
supply cahin attack
# Types of Malware
- [ ] Trojans  
- [ ] Viruses  
- [ ] Ransomware  
- [ ] Computer Worms  
- [ ] Rootkits  
- [ ] PUAs or Grayware  
- [ ] Spyware  
- [ ] Keylogger  
- [ ] Botnets  
- [ ] Fileless Malware



