# network-scan
# Task 1 - Local Network Port Scanning

## Objective
Use Nmap to scan the local network and identify open ports and services to understand network exposure.

## Tools Used
- Nmap
- Kali Linux

## Network Range
`192.168.1.0/24` 

## Summary of Hosts Found & Screenshots
- Total hosts up: 13
- ![Full Network Scan](screenshot_full_scan.png)
![Host 192.168.1.1](screenshot_host_192.168.1.1.png)
![Host 192.168.1.11](screenshot_host_192.168.1.11.png)
![Host 192.168.1.40](screenshot_host_192.168.1.40.png)


## Detailed Findings

### 192.168.1.1 (RTK_GW)
- Open Ports: 53, 80, 443
- Services:
  - DNS: dnsmasq 2.45
  - HTTP/HTTPS: Boa HTTPd 0.93.15 (vulnerable)
- Notes: Admin panel exposed; outdated server software

### 192.168.1.11 
- Open Port: 7070 (ssl/realserver?)
- Notes: Unknown service, possibly media or IoT device

### 192.168.1.40 (V2031)
- No open ports, but filtered services on 1719 and 1720 (VoIP)

## Conclusion
The network has a mix of devices, with some running outdated or unidentified services. Proper segmentation and port restriction are recommended.
