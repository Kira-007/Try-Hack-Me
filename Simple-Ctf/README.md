# Simple CTF writeup
The first task when beggining a CTF is enumeration

## Nmap 
```bash
namp -T4 -sV 10.10.114.166
```
The Nmap flag ```-sV``` is useful as it returns details to do with the versions of services running on the target 

```
PORT     STATE SERVICE VERSION
21/tcp   open  ftp     vsftpd 3.0.3
80/tcp   open  http    Apache httpd 2.4.18 ((Ubuntu))
2222/tcp open  ssh     OpenSSH 7.2p2 Ubuntu 4ubuntu2.8 (Ubuntu Linux; protocol 2.0)
```
We have found 3 ports 21, 80, 2222. 

lets start exploring ports one by one 

## Port 21: ftp
The ftp server running on target vulnerable to Anonymous login


## Gobuster
```

```
### How many services are running under port 1000?
> 2

### What is running on the higher port?
> ssh

### What's the CVE you're using against the application?
> CVE-2019-9053

### To what kind of vulnerability is the application vulnerable?
> sqli

### What's the password?
> secret

### Where can you loginwith the details obtained?
> ssh

### What's the user flag?
> G00d j0b, keep up!

### Is there any other user in the home directory? What's its name?
> sunbath

### What can you leverage to spawn a privileged shell?
> vim

### What's the root flag?
> W3ll d0n3. You made it!
