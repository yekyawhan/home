---
{"tags":["dockerio"],"dg-publish":true,"permalink":"/docker/calibre-web-for-ebook-read/","dgPassFrontmatter":true,"noteIcon":""}
---


not good 

[![Main screen](https://github.com/janeczku/calibre-web/wiki/images/main_screen.png)](https://github.com/janeczku/calibre-web/wiki/images/main_screen.png)

## [Features](https://github.com/janeczku/calibre-web#features)

- Modern and responsive Bootstrap 3 HTML5 interface
- Full graphical setup
- Comprehensive user management with fine-grained per-user permissions
- Admin interface
- Multilingual user interface supporting 20+ languages ([supported languages](https://github.com/janeczku/calibre-web/wiki/Translation-Status))
- OPDS feed for eBook reader apps
- Advanced search and filtering options
- Custom book collection (shelves) creation
- eBook metadata editing and deletion support
- Metadata download from various sources (extensible via plugins)
- eBook conversion through Calibre binaries
- eBook download restriction to logged-in users
- Public user registration support
- Send eBooks to E-Readers with a single click
- Sync Kobo devices with your Calibre library
- In-browser eBook reading support for multiple formats
- Upload new books in various formats, including audio formats
- Calibre Custom Columns support
- Content hiding based on categories and Custom Column content per user
- Self-update capability
- "Magic Link" login for easy access on eReaders
- LDAP, Google/GitHub OAuth, and proxy authentication support



1. Open your browser and navigate to `http://localhost:8083` or `http://localhost:8083/opds` for the OPDS catalog
2. Log in with the default admin credentials
3. If you don't have a Calibre database, you can use [this database](https://github.com/janeczku/calibre-web/raw/master/library/metadata.db) (move it out of the Calibre-Web folder to prevent overwriting during updates)
4. Set `Location of Calibre database` to the path of the folder containing your Calibre library (metadata.db) and click "Save"
5. Optionally, use Google Drive to host your Calibre library by following the [Google Drive integration guide](https://github.com/janeczku/calibre-web/wiki/G-Drive-Setup#using-google-drive-integration)
6. Configure your Calibre-Web instance via the admin page, referring to the [Basic Configuration](https://github.com/janeczku/calibre-web/wiki/Configuration#basic-configuration) and [UI Configuration](https://github.com/janeczku/calibre-web/wiki/Configuration#ui-configuration) guides

#### [Default Admin Login:](https://github.com/janeczku/calibre-web#default-admin-login)

- **Username:** admin
- **Password:** admin123

## [Docker Images](https://github.com/janeczku/calibre-web#docker-images)

- [Docker Hub](https://hub.docker.com/r/linuxserver/calibre-web)

```dockercli
docker run -d \
--name=calibre-web \
-e PUID=1000 \
-e PGID=1001 \
-e TZ=Asia/Yangon \
-p 8083:8083 \
-v /mnt/data:/config \
-v /mnt/ebook:/books \
--restart unless-stopped \
lscr.io/linuxserver/calibre-web:latest
```



