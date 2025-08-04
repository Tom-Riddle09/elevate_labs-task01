# Elevate Labs - Task 01 

## OBJECTIVE
Perform port scan of home network - find connected hosts and open ports.  
Capture ip packets using Wireshark and observe traffic.  

## HOSTS & PORTS FOUND
Scan performed: nmap -sS 192.168.1.0/24  
192.168.1.1 : port 53, 80, 443, 5555 are open  
192.168.1.5: port 1152, 7201, 14442, 32772, 44442, 58080 are filtered  
192.168.1.13: All 1000 scanned ports are in ignored state ( possibly filtered - no response)  
192.168.1.10: All 1000 scanned ports are in ignored state ( possibly filtered - no response)  
192.168.1.10: 999 ports closed, port 22 open.   

## Common Services Running on Open Ports
53 (TCP\UDP) : DNS  
22 : SSH  
80 : HTTP (Web)  
443 : HTTPS (Secure Web)  
5555 : ADB (Android Debug Brigde) or custom services  

## Security Risks due to Open Ports
Port 53: if DNS is misconfigured or externally exposed, it can be abused for DNS amplification DDoS.  
Port 80: Unencrypted - vulnerable to MITM, sniffing, or old vulnerable web interfaces.  
Port 5555: if ADB, Potential High risk - allows remote shell access to Android-based devices.  
Port 22: Potential Brute-force attack risk, should be hardened with key-based auth, disable root login.  

### Scan Result Screenshots are added to the repository. 
