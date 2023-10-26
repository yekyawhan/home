---
{"tags":["dockerio"],"dg-publish":true,"permalink":"/docker/prowlarr-install-docker/","dgPassFrontmatter":true,"noteIcon":""}
---


### [docker-compose (recommended,](https://github.com/linuxserver/docker-prowlarr#docker-compose-recommended-click-here-for-more-info) [click here for more info](https://docs.linuxserver.io/general/docker-compose))

```yaml
---
version: "2.1"
services:
  prowlarr:
    image: lscr.io/linuxserver/prowlarr:latest
    container_name: prowlarr
    environment:
      - PUID=1000
      - PGID=1000
      - TZ=Etc/UTC
    volumes:
      - /path/to/data:/config
    ports:
      - 9696:9696
    restart: unless-stopped
```

### [docker cli (](https://github.com/linuxserver/docker-prowlarr#docker-cli-click-here-for-more-info)[click here for more info](https://docs.docker.com/engine/reference/commandline/cli/))

```shell
docker run -d \
  --name=prowlarr \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=Etc/UTC \
  -p 9696:9696 \
  -v /path/to/data:/config \
  --restart unless-stopped \
  lscr.io/linuxserver/prowlarr:latest
```
