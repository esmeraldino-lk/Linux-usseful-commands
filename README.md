# Linux-usseful-commands
Personal repository for linux commands


netstat -rn 
>Show active network disponibility
>![image](https://github.com/esmeraldino-lk/Linux-usseful-commands/assets/133903212/1c5d8aae-c2e7-4e6e-a237-f18bccd9de85)


tree
>Make a tree for folder path
>![image](https://github.com/esmeraldino-lk/Linux-usseful-commands/assets/133903212/d5109cec-91f0-4d0a-8c22-8a84beb3a512)


arp -a IP_ADDRESS 
>Show MAC from IP LAN
>![image](https://github.com/esmeraldino-lk/Linux-usseful-commands/assets/133903212/d2fc4ff4-a3ae-4c20-bdec-2957ea4d78f2)


## Scanning

###WEB SCAN
Whatweb http://94.237.62.2/
> out-> http://94.237.62.2 [301 Moved Permanently] Country[FINLAND][FI], IP[94.237.62.2], RedirectLocation[https://94.237.62.2/]

###LISTS
SecLists
> [!NOTE]
> Main list for brute force
![image](https://github.com/esmeraldino-lk/Linux-usseful-commands/assets/133903212/e4cde0a2-d9f3-4661-92ef-230bfe497555)


###SAMBA SCAN
smbclient
> Used for access smb

###SCAN PORTS
nmap -sC -sV -p21 [IP or URL]
> Scan ports
> -sC -> Scan with script default
> -sV -> Scan version and service
> -p21 -> port 21

###WEB ENUMERATION
gobuster -m [MODE] -u [URL] -w [LIST]
> Enumeration

###OTHERS
SITE.COM\robots.txt
> User-agend: *
> Used for disallowed paths

