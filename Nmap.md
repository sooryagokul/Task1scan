
I am using Kali Linux, which comes with Nmap pre-installed. Kali is a widely-used Linux distribution for penetration testing and security auditing.

About Nmap:
Nmap (Network Mapper) is an open-source tool used for:
 - Network discovery

 - Port scanning

 -Vulnerability detection

It helps identify hosts, open ports, services, operating systems, and potential security risks in a network.

Official site:  https://nmap.org

    ------------------------------------------------------------------------------------------------------------------

To determine the IP range of my local network, I used the ipconfig command on Windows CMD:

<img width="1172" height="817" alt="ipconfig" src="https://github.com/user-attachments/assets/8936d6ff-5309-47f9-b506-1ff795948db0" />

" ipconfig "

From the output, I found my local IP address and subnet (e.g., 192.168.18.101), which helped me identify the full range:
-->  192.168.18.0/24

This range includes all devices on the local network from 192.168.18.1 to 192.168.18.254.


     ------------------------------------------------------------------------------------------------------------------


Perform TCP SYN Scan using Nmap : 

To discover active hosts and open ports on the local network, I performed a TCP SYN scan using the following command:

     " nmap -sS 192.168.18.101/24 "

 
-sS: Performs a SYN scan (also called half-open scanning), which is stealthier and faster  than a full TCP connection.

192.168.18.101/24: Scans the entire subnet, targeting all IPs from 192.168.18.1 to 192.168.18.254.

and then ,
 
      nmap -sS 192.168.18.101/24 -oN scan_results.txt (to save the scan results)  



    ------------------------------------------------------------------------------------------------------------------

    
