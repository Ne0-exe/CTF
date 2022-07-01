**Walkthrough of LazyAdmin CTF by vintage_exe**

IP of the machine: 10.10.34.55

Nmap scan: 

# Nmap 7.92 scan initiated Tue Jun 28 12:42:19 2022 as: nmap -sV -vv -oN walkthrough.md 10.10.34.55
Nmap scan report for 10.10.34.55
Host is up, received echo-reply ttl 63 (0.053s latency).
Scanned at 2022-06-28 12:42:20 CEST for 8s
Not shown: 998 closed tcp ports (reset)
PORT   STATE SERVICE REASON         VERSION
22/tcp open  ssh     syn-ack ttl 63 OpenSSH 7.2p2 Ubuntu 4ubuntu2.8 (Ubuntu Linux; protocol 2.0)
80/tcp open  http    syn-ack ttl 63 Apache httpd 2.4.18 ((Ubuntu))
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Tue Jun 28 12:42:28 2022 -- 1 IP address (1 host up) scanned in 8.52 seconds

Dirbuster:

/content directory had this entry on the site: *Welcome to SweetRice - Thank your for install SweetRice as your website management system.*
/content/inc/mysql_backup/ directory seems interesting

"passwd\\";s:32:\\"42f749ade7f9e195bf475f37a44cafcb\\" <----There it is

42f749ade7f9e195bf475f37a44cafcb----------MD5---------> Password123

In /content/as directory we can find login panel.
Username: manager
Password: Password123

There we can find out that the version is 1.5.1 so let's find the exploits.
SweetRice 1.5.1 - Cross-Site Request Forgery / PHP Code Execution look nice
Executing reverse shell by pentestmonkey i was able to get the shell and gain user's flag. **THM{63e5bce9271952aad1113b6f1ac28a07}**
Now it was time to gain root privileges.

Using perl and modyfying backup.pl I was able to gain root accout and in /root directory was root's flag.