---
{"tags":["cct"],"Date":["\"15th Wednesday, November  2023, 10:07 pm\""],"status":null,"cssclasses":null,"dg-publish":true,"permalink":"/cct-online-training/module-1/","dgPassFrontmatter":true,"noteIcon":""}
---



### Information Security Threats and Vulnerabilities


> [!tip]+ Module Objectives
> Understanding the Threat and Threat Sources
> Understanding the Threat Actors/Agents
> Understanding Various Threat Vectors
> Overview of t he Malware and t he Common Techniques Attackers Use to Distribute Malware
> Understanding t he Different Types of Malware
> Understanding the Vulnerability and Examples of Network Security Vulnerabilities
> Overview of the Common Areas of Vulnerability
> Understanding t he Impact of Vulnerabilities
> Understanding t he Risk of Vulnerabilities
> Understanding t he Classification of Vulnerabilities 

### Threat Sources
![Threat Sources.png|undefined](/img/user/Images%20All/cct-images/Threat%20Sources.png)


```ad-bug
collapse: open
title: Components of Malware
■ Crypter: Software that protects malware from undergoing reverse engin eer ing or analysis.  
■ Downloader: A type of Trojan t hat downloads other malware from the Int ernet on to the PC.  
■ Dropper: A type of Troj an that covertly installs other malware files on to the system.  
■ Exploit: A malicious code that b reaches t he system securi ty via software vulnerabilities to access informat io n or  
install malware
■ Injector: A program that injects its code in to other vulnerable running processes and changes how th ey exec ute to  
hide or prevent its removal.  
■ Obfuscator: It is a program that conceals the malicious code of malware via various  
techniques, thus making it difficult for security mechanisms to detect or remove it.  
■ Packer: A program that allows all files to bundle t ogether into a single executab le fi le via compression to bypass  
security software detection.  
■ Payload: A piece of software that allows control over a computer system after it has been exploited.  
■ Malicious Code: A command that defines malware's basic functionalities such as stealing data and creating backdoors:  
o Java Applets  
o ActiveX Controls  
o Browser Plug-ins  
o Pushed Content	 
```

# Types of Malware
```ad-bug
collapse: open
title: Types of Malware  
A malware is a piece of malicious software that is designed to perform activities intended by  
the attacker without user consent. It may be in the form of executable code, active content,  
scripts, or other kinds of software.  
Listed below are various type s of malware:  
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

```


```ad-bug
title: Types ofTrojans (1)
collapse: open 
#### Trojans are categories according to their functioning and targets  
Some of the example includes:  
1 Remote Access Trojans 8 Service Protocol Trojans  
2 Backdoor Trojans 9 Mobile Trojans  
3 Botnet Trojans 10 loT Trojans  
4 Rootkit Trojans 11 Security Software Disabler Trojans  
5 E- Banking Trojans 12 Destructive Trojans  
6 Point-of- Sale Trojans 13 DDoS Attack Trojans  
7 Defacement Trojans 14 Command Shell Trojans

```
စာမျက်နှာ-43-စာရွက်-58

```ad-caution
title: Creating a Trojan
collapse: open
Some additional Trojan horse construction kit s are as follows:  
- [ ] DarkHorse Trojan Virus Maker  
- [ ] Trojan Horse Construction Kit  
- [ ] Senna Spy Trojan Generator  
- [ ] Batch Trojan Generator  
■ Umbra Loader - Botnet Trojan Maker  
Exam 212-82  
Module 01 Page 46 
```
![Creating a Trojan.png|undefined](/img/user/Images%20All/cct-images/Creating%20a%20Trojan.png)

```ad-bug
title: What is a Virus? (2)
- [ ] Infects other programs  
- [ ] Transforms itself  
- [ ] Encrypts it self  
- [ ] Alters data  
- [ ] Corrupts files and programs  
- [ ] Replicates itself
```

```
Purpose of Creating Viruses
 Inflict damage on competitors  
 Realize financial benefits  
 Vandalize intellectual property  
 Play pranks  
 Conduct research  
 Engage in cyber-terrorism  
 Distribute polit ical messages  
 Damage network s or computers  
 Gain remote access to a victim's computer 
 Module 01 Page 51
```

![Purpose of Creating Viruses.png|undefined](/img/user/Images%20All/cct-images/Purpose%20of%20Creating%20Viruses.png)

![Indicaations of virus attack.png|undefined](/img/user/Images%20All/cct-images/Indicaations%20of%20virus%20attack.png)

![stages of virus lifecycle.png|undefined](/img/user/Images%20All/cct-images/stages%20of%20virus%20lifecycle.png)
![Computer Get Infected by Viruses.png|undefined](/img/user/Images%20All/cct-images/Computer%20Get%20Infected%20by%20Viruses.png)
![Types of viruses.png|undefined](/img/user/Images%20All/cct-images/Types%20of%20viruses.png) 


#virusmakertools
```ad-error
title: Virus Maker Tools
- [ ] DELmE's Batch Virus Maker
- [ ] JPS Virus Maker
- [ ] Bhavesh Virus Maker SlW  
- [ ] Deadly Virus Maker  
- [ ] SonicBat Batch Virus Maker  
- [ ] Tera BIT Virus Maker  
- [ ] AndreinickOS's Batch Virus Maker
```

# Ransom ware (3)

![Pasted image 20231119034722.png|undefined](/img/user/Images%20All/cct-images/Pasted%20image%2020231119034722.png) 

# worm (4)
![Pasted image 20231119035830.png|undefined](/img/user/Images%20All/cct-images/Pasted%20image%2020231119035830.png)


## Different Between Worm & Virus
>[!multi-column]
>>[!todo]+ Virus
>>- A virus infects a system by inserting it self into a file or executable program
>>- It might de l ete or alter the content of files or change the location of files in the system
>>- It alters the way a computer system operates without the knowledge or consent of a user
>>- A virus cannot spread to other computers unless an infected fi le is repl icated and sent to the other computers
>>- A virus spreads at a uniform rate, as programmed 
>>- Viruses are difficult to remove from infected machines
>
>>[!info]+ worm
>>- A worm infects a system by exploiting a vulnerability in an OS or application by replicating itself
>>- Typically, a worm does not modify any stored programs; it only exploits t he CPU and memory
>>- It consumes network bandwidth, system memory, etc., excessively over loading servers and computer of a user systems
>>- A worm can replicate itself and spread using IRC, Outlook, or other applicable mailing programs after installation in a system
>>- A worm spreads more rapid ly than a virus
>>- Compared with a virus, a worm can be removed machines easily from a system
>
>> [!danger]+ Computer Worms
>> Attackers use worm pa yloads to install backdoors on infected computers, which turns them into zombies and creates a botnet. Attacker s use these botnets to initiate cyber-attacks. Some of the latest computer worms are as follows:
>> - [ ]  Manero
>> - [ ]  Bondat
>> - [ ]  Beapy
>
>>[!bug]+  Worm Makers
>>- [ ] Internet Worm Maker Thing
>>- [ ] Batch Worm Generator
>>- [ ] C++ Worm Generator
---


> [!multi-column]
>
>> [!note]+ ## Rootkits (5)
>>- Rootkits are programs that **hide their presence** as well as attacker's malicious activities, granting them full access to the server or host at that time, and in the future 
>>- Rootkits replace certain operating system calls and utilities with their ow n **modified versions** of those routines that, in turn, undermine the security of the target system causing malicious functions to be executed 
>>- A typical rootkit comprises of backdoor programs, DDoS programs, packet sniffers, log-wiping utilities, I RC bots, etc.
>
>> [!note]+ The attacker places a rootltit by
>>□ Scanning for **vulnerable** computers and servers on the web 
>>□ **Wrapping** it in a special package like a game 
>>□ Installing it on public computers or corporate computers through **social engineering** 
>>□ Launching a **zero-day attack** (privilege escalation, buffer overflow, Windows kernel exploitation, etc.)
>
>> [!note]+ Objectives of a rootkit:
>> □ To **root** the host system and **gain remote backdoor** access 
>> □ To mask **attacker tracks** and presence of malicious applications or processes 
>> □ To gather **sensitive data, network traffic**, etc. from the system to which attackers might be restricted or possess no access 
>> □ To store other **malicious programs** on the system and act as a server resource for bot updates
>
>>[!tip]+ Popular Rootkits
>>- [ ] LoJax is a type of UEFI rootkit that is widely used by attackers to perform cyber-attacks. LoJax is created to inject malware into the system and is automatically executed whenever the system starts up. It exploits UEFI, which acts as an interface between the OS and the firmware. It is extremely challenging to detect LoJax as it evades traditional security controls and maintains its persistence even after OS reinstallation or hard disk replacement
>>- [ ] Scranos is a trojanized rootkit that masquerades as cracked software or a legitimate application, such as anti-malware, a video player, or an ebook reader, to infect systems and perform data exfiltration that damages the reputation of the target and steals intellectual property. When this rootkit executed, a rootkit driver is automatically installed, which then starts installing other malicious components into the system. Apart from installing malicious components, Scranos also interacts with various websites on the behalf of the victim
>>**Module 01 Page 76**
---

# PUAs or Grayware (6)

![Pasted image 20231119044359.png|600](/img/user/Images%20All/cct-images/Pasted%20image%2020231119044359.png) ![Pasted image 20231119044420.png|600](/img/user/Images%20All/cct-images/Pasted%20image%2020231119044420.png)

---
# Spyware(7)

![Pasted image 20231119044750.png|650](/img/user/Images%20All/cct-images/Pasted%20image%2020231119044750.png) ![Pasted image 20231119044820.png|650](/img/user/Images%20All/cct-images/Pasted%20image%2020231119044820.png)





