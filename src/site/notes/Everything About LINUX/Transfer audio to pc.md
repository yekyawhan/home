---
{"tags":["ffmpeg"],"dg-publish":true,"permalink":"/everything-about-linux/transfer-audio-to-pc/","dgPassFrontmatter":true,"noteIcon":""}
---

0# Linux (transmitter) side:
### sudo ဖြင့် ဖွင့်မရပါ ရိုးရိုး အကောင့်နှင့်သာရသည်
```
sudo apt install pulseaudio-utils
```
```
sudo apt install ffmpeg
nano audiotransfer.sh
```
```shell
#!/bin/bash
pactl load-module module-null-sink sink_name=remote 
ffmpeg -f pulse -i "remote.monitor" -ac 2 -acodec pcm_s16le -ar 48000 -f s16le "udp://192.168.0.6:18181"
```
or
```shell
pactl load-module module-null-sink sink_name=remote
ffmpeg -f pulse -i "remote.monitor" -ac 2 -acodec pcm_u8 -ar 48000 -f u8 "udp://RECEIVER:18181"
```
---
# Windows (receiver) side:
```
ffplay -nodisp -ac 2 -acodec pcm_s16le -ar 48000 -analyzeduration 0 -probesize 32 -f s16le -i udp://0.0.0.0:18181?listen=1
```
or
```
ffplay.exe -nodisp -ac 2 -acodec pcm_u8 -ar 48000 -analyzeduration 0 -probesize 32 -f u8 -i udp://0.0.0.0:18181?listen=1
```
---
### vbs script create
### Require: JDK 1.8 on my system
```
Set WshShell = CreateObject("WScript.Shell")         
WshShell.Run chr(34) & "C:\Audiorecive\audiorecive.bat" & Chr(34), 0        
Set WshShell = Nothing
```
---
### Stream from player
```
ffmpeg -i rtp://192.168.0.6"18181 -acodec pcm_s16le -ar 44100 -f wav - | "C:\Program Files\DAUM\PotPlayer\PotPlayerMini64.exe" -
```
```
ffmpeg -i rtp://192.168.0.134:18181 -acodec pcm_s16le -ar 44100 -f wav - | "C:\Program Files\DAUM\PotPlayer\PotPlayerMini64.exe" -
```
---
### auto run app
```
create file on
~/.config/autostart/barrier.desktop
nano audiotransfer.desktop

[Desktop Entry]
Type=Application
Name=ffmpeg
Exec=/home/y3kh/program/audio-transfer/audiotransfer.sh
StartupNotify=true
Terminal=true

chmod  +x barrier.desktop
```
---

#### You have -f u8 but the documentation seems to indicate -sample_fmt u8, yet when tried it doesn't work.
#### Why does -f u16 not work for 16 bit sound?
#### How are there 2 -f options on the same line?
#### Where did you learn about -analyzeduration 0 and -probesize 32 ? I can't find them documented.

----
search device id
```bash
ffmpeg -list_devices true -f dshow -i dummy
```
### this is my hardware devices

[dshow @ 0000029026cbd9c0] Could not enumerate video devices (or none found).
[dshow @ 0000029026cbd9c0] "Microphone (Realtek(R) Audio)" (audio)
[dshow @ 0000029026cbd9c0]   Alternative name "@device_cm_{33D9A762-90C8-11D0-BD43-00A0C911CE86}\wave_{DB0F4F69-E718-42E4-BA1F-39A2E48EEEF5}"
[dshow @ 0000029026cbd9c0] "CABLE Output (VB-Audio Virtual Cable)" (audio)
[dshow @ 0000029026cbd9c0]   Alternative name "@device_cm_{33D9A762-90C8-11D0-BD43-00A0C911CE86}\wave_{19C5DB65-6C6F-488D-AE73-5B9B02966D39}"
[dshow @ 0000029026cbd9c0] "VoiceMeeter Output (VB-Audio VoiceMeeter VAIO)" (audio)
[dshow @ 0000029026cbd9c0]   Alternative name "@device_cm_{33D9A762-90C8-11D0-BD43-00A0C911CE86}\wave_{B79C4992-8475-42F5-946A-1DE8D325A86B}"
[dshow @ 0000029026cbd9c0] "VoiceMeeter Aux Output (VB-Audio VoiceMeeter AUX VAIO)" (audio)
[dshow @ 0000029026cbd9c0]   Alternative name "@device_cm_{33D9A762-90C8-11D0-BD43-00A0C911CE86}\wave_{FE541D70-B4E2-44F6-ACD3-B599C13F42AC}"
[in#0 @ 0000029026cbd800] Error opening input: Immediate exit requested