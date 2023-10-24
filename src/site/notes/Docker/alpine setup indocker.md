---
{"tags":["dockerio"],"dg-publish":true,"permalink":"/docker/alpine-setup-indocker/","dgPassFrontmatter":true,"noteIcon":""}
---



```
 docker container run -p 22533:22533 -it --name alpine2 alpine /bin/sh
```




### shell zsh setup power10k

```
apk add zsh zsh-theme-powerlevel10k
mkdir -p ~/.local/share/zsh/plugins
ln -s /usr/share/zsh/plugins/powerlevel10k ~/.local/share/zsh/plugins/
```
