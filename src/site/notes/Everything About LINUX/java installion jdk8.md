---
{"tags":["Java"],"dg-publish":true,"permalink":"/everything-about-linux/java-installion-jdk8/","dgPassFrontmatter":true,"noteIcon":""}
---


```
sudo update-alternatives --config java       
```
### download java from site only java 8

```
apt install default-jre              # version 2:1.11-72, or
apt install openjdk-11-jre-headless  # version 11.0.20.1+1-0ubuntu1~20.04
apt install openjdk-13-jre-headless  # version 13.0.7+5-0ubuntu1~20.04
apt install openjdk-16-jre-headless  # version 16.0.1+9-1~20.04
apt install openjdk-17-jre-headless  # version 17.0.8.1+1~us1-0ubuntu1~20.04
apt install openjdk-8-jre-headless   # version 8u382-ga-1~20.04.1

```
		terminal 
		java --version
		cd /usr/lib/jvm
		sudo tar -xvzf ~/Downloads/jdk-8u201-linux-x64.tar.gz
		cd /usr/lib/jvm/jdk1.8.0_201
		sudo nano /etc/enviroment
		(add to path)
		:/usr/lib/jvm/jdk1.8.0_201/bin:/usr/lib/jvm/jdk1.8.0_201/db/bin:/usr/lib/jvm/jdk1.8.0_201/jre/bin/
	
		sudo update-alternatives --install "/usr/bin/java" "java" "/usr/lib/jvm/jdk1.8.0_201/jre/bin/java" 1711
	
		sudo update-alternatives --install "/usr/bin/java" "java" "/usr/lib/jvm/jdk1.8.0_201/bin/javac" 1711
	
		sudo update-alternatives --set java /usr/lib/jvm/jdk1.8.0_201/bin/javac
		sudo update-alternatives --config java                                 
		choose 2
		java -version
	
	
	:/usr/lib/jvm/java-1.8.0-openjdk-amd64/bin:/usr/lib/jvm/jdk1.8.0_201/db/bin:/usr/lib/jvm/java-1.8.0-openjdk-amd64/jre/bin/
	
	
	/usr/lib/jvm/java-1.8.0-openjdk-amd64
	

			mousepad /etc/enviroment
			J2SDKDIR="/usr/lib/jvm/jdk1.8.0_381"
			J2REDIR="/usr/lib/jvm/jdk1.8.0_381jre"
			JAVA HOME="/usr/lib/jvm/jdk1.8.0_381"
			DERBY HOME="/usr/lib/jvm/jdk1.8.0_381/db"

	sudo update-alternatives --install "/usr/bin/java" "java" "/usr/lib/jvm/jdk1.8.0_381/jre/bin/java" 0		
	sudo update-alternatives --install "/usr/bin/java" "javac" "/usr/lib/jvm/jdk1.8.0_381/bin/javac" 0
	sudo update-alternatives --set java /usr/lib/jvm/jdk1.8.0_381/bin/java
	sudo update-alternatives --set javac /usr/lib/jvm/jdk1.8.0_381/bin/javac
```
sudo update-alternatives --config java       
```
alpine os

	apk add openjdk8
	java -version
	