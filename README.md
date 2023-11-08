# Linux-usseful-commands
Personal repository for linux commands

## GENERAL

netstat -rn 

>Show active network disponibility


![image](https://github.com/esmeraldino-lk/Linux-usseful-commands/assets/133903212/1c5d8aae-c2e7-4e6e-a237-f18bccd9de85)


tree

>Make a tree for folder path


![image](https://github.com/esmeraldino-lk/Linux-usseful-commands/assets/133903212/d5109cec-91f0-4d0a-8c22-8a84beb3a512)


arp -a IP_ADDRESS 

>Show MAC from IP LAN


![image](https://github.com/esmeraldino-lk/Linux-usseful-commands/assets/133903212/d2fc4ff4-a3ae-4c20-bdec-2957ea4d78f2)


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
´´´
sudo apt-get install build-essential zlib1g zlib1g-dev libxml2 libxml2-dev libxslt-dev locate libreadline6-dev libcurl4-openssl-dev git-core autoconf curl postgresql postgresql-contrib libpq-dev libapr1 libaprutil1 libsvn1 libpcap-dev -y && git clone https://github.com/rapid7/metasploit-framework.git && cd metasploit-framework && sudo bash -c 'for MSF in $(ls msf*); do ln -s /usr/local/src/metasploit-framework/$MSF /usr/local/bin/$MSF;done' && sudo service postgresql start && sudo msfdb init
´´´


