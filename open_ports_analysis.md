
scanned 192.168.18.0/24  using " nmap -sS 192.168.18.101/24 "  and found:


<img width="1072" height="602" alt="nmap" src="https://github.com/user-attachments/assets/e69e7262-c966-4546-a0d4-88547b8824a8" />


* port 53 - open -  DNS Service (domain)

  port 80 - open -  HTTP Web Service

 These are open ports – they accepted your SYN request (responded with SYN-ACK).

* Other hosts had all ports filtered or unresponsive, which could mean:

  Firewall blocking the scan , Host not running any visible services ,Host unreachable on  those ports


* Port 53/tcp → DNS Service (domain)  

  Usually runs on DNS servers

  Might be providing DNS resolution for devices on the network

  Could be vulnerable to DNS cache poisoning or amplification attacks if misconfigured

* Port 80/tcp → HTTP Web Service

  This is a web server (unsecured – no HTTPS)
  
  Potential risks are :

     Unauthenticated admin panels

     Directory traversal

     Outdated web apps
