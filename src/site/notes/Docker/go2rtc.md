---
{"dg-publish":true,"permalink":"/docker/go2rtc/","dgPassFrontmatter":true,"noteIcon":""}
---

plug in hos is better now 
1 add repo first
```
https://github.com/AlexxIT/hassio-addons
```
and resping or apk update && apk upgrade
search on add on store go2rtc

If you want to install on Docker try is below
--
There are two versions of the Docker container and Hass Add-on:
- Latest (alpine) support hardware acceleration for Intel iGPU (CPU with Graphics) and Raspberry.
- Hardware (debian 12) support Intel iGPU, AMD GPU, NVidia GPU.
```
docker pull alexxit/go2rtc
```
just draw by gui
or
you don't need docker compose


```
nano docker-compose.yaml
```
```
services:
  go2rtc:
    image: alexxit/go2rtc
    network_mode: host       # important for WebRTC, HomeKit, UDP cameras
    privileged: true         # only for FFmpeg hardware transcoding
    restart: unless-stopped  # autorestart on fail or config change from WebUI
    environment:
      - Asia/Yangon  # timezone in logs
    volumes:
      - "~/go2rtc:/config"   # folder for go2rtc.yaml file (edit from WebUI)
```

or 
you can try with pve helper on site
