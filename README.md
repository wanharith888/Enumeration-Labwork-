**Challenge 1**

<img width="1050" height="922" alt="image" src="https://github.com/user-attachments/assets/bd83d473-be06-4d4e-ad4c-6d06da221d1d" />


I used the nbtstat -a command to retrieve the NetBIOS name table from a remote target, which helps identify the machine's role on the network.


**Challenge 2**


<img width="634" height="172" alt="image" src="https://github.com/user-attachments/assets/c9aa256b-73cb-4c74-abde-1e28f2708b5e" />


I executed nmap -F to perform a fast scan, which limits the discovery to the top 100 most common ports rather than the full range of 1,000. This command allows me to quickly identify active services like SSH or HTTP on the target machine without generating excessive network traffic.


**Challenge 3**


<img width="780" height="757" alt="image" src="https://github.com/user-attachments/assets/68270bc0-0cf6-4f00-b643-9100f42b7381" />


I utilized **nslookup** and **dig** to query public DNS records, which allowed me to map out a domain's infrastructure by identifying its IP addresses and mail servers. By specifically requesting **MX** and **ANY** records, I can uncover critical details about the organization's mail handling and various other resource records vital for network reconnaissance.


**Challenge 5**


<img width="506" height="385" alt="image" src="https://github.com/user-attachments/assets/fe913226-e0ed-42e4-8fb7-423d7be9a775" />


By analyzing the Time to Live (TTL) value of 64 from the ping output, I can infer that the target host is likely running a Linux or Unix-based operating system.


**Challenge 9**


<img width="211" height="83" alt="image" src="https://github.com/user-attachments/assets/7664a514-6efe-40f1-a82a-f14834b4c81c" />


I used nc (Netcat) to connect to port 21, which allowed me to capture the FTP service banner and identify the specific software version running.


**Challenge 10**


<img width="495" height="310" alt="image" src="https://github.com/user-attachments/assets/67cf5df8-3315-4c16-9bbf-685ab6fba00a" />


I used the **ftp** command to attempt a connection and successfully logged in using the "anonymous" username, which confirms a significant security misconfiguration on the target. This access allowed me to list and browse readable directories.


**Challenge 11**


<img width="556" height="336" alt="image" src="https://github.com/user-attachments/assets/0e0af1c5-bef8-4ce7-ac50-434790461b8b" />

<img width="565" height="792" alt="image" src="https://github.com/user-attachments/assets/552b1f14-72fb-403e-9af6-c1005970bc47" />

<img width="563" height="800" alt="image" src="https://github.com/user-attachments/assets/5dc1adff-8bba-46d6-8722-7b2b8c693322" />


I utilized Nmap Scripting Engine (NSE) scripts to probe port 445, successfully extracting detailed OS information and the domain name from the target's SMB service. By running the user enumeration script, I was also able to compile a list of valid accounts, such as Administrator and Guest, which are critical for identifying potential targets for credential-based attacks.


**Challenge 16**


<img width="992" height="617" alt="image" src="https://github.com/user-attachments/assets/145111d0-8c9d-42f2-a6d8-9b6f7819d761" />


I ran nmap -sV to probe open ports and determine the exact service names and version numbers for protocols like SSH, HTTP, and FTP.


**Challenge 19**


<img width="376" height="415" alt="image" src="https://github.com/user-attachments/assets/a69d5b82-7f1d-4549-9580-fc7fb97cfac2" />


I used the rpcinfo -p command to query the portmapper on the target, which revealed a list of registered Remote Procedure Call (RPC) services and their respective port numbers.


**Challenge 27**


<img width="747" height="340" alt="image" src="https://github.com/user-attachments/assets/00178f28-d638-4694-9c0f-0bba19619c53" />


I used the nmap -6 -O command to perform OS detection specifically over IPv6, which is essential for identifying targets that might have different security configurations than their IPv4 counterparts. This allows me to verify open v6-enabled services and obtain an OS guess, ensuring a comprehensive view of the network's addressable surface.


**Challenge 29**


<img width="637" height="486" alt="image" src="https://github.com/user-attachments/assets/bc0ba7cc-c33b-43b5-95f7-bd9e45f0efc4" />


I employed Nmap scripts against port 25 to test for common SMTP misconfigurations, specifically attempting to enumerate valid system usernames and check if the server acts as an open relay.
