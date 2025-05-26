# Cybersecurity Task 1: Port Scanning with Nmap #

## Tools Used:
- WINDOW 10
- CMD
- NMAP

## My Local IP Info:
- IP: 192.168.1.39
- Subnet: 255.255.255.0
- Scanned range: 192.168.1.0/24

## Nmap Command Used: 
              TARGET:192.168.1.39                   PROFILE:  Intense scan
             COMMAND:NMAP -sS 192.168.1.39
             
## Summary:
- Found 5 devices online.
- Discovered open ports: 135, 139, 445, 902, 912
- Used Wireshark to verify SYN packets.

## Risks:
- Open RDP (3389) port is dangerous if not protected.
 Open RDP (Remote Desktop Protocol) – Port 3389
 Dangerous if not protected.
 This port is not listed in your summary but commonly targeted by attackers. If you meant to refer to  RDP, confirm whether port 3389 is open.
 Mitigation: Use firewalls, Network Level Authentication (NLA), and strong credentials or VPN access.

- SSH (22) must use strong passwords.
  SSH (Secure Shell) – Port 22
  Must use strong passwords or key-based authentication.
  This port is not in your open port list, but if SSH is used, ensure proper security measures:
  Disable password login if possible (use SSH keys).
  Restrict login access (e.g., only allow specific IPs).
  Use fail2ban or similar intrusion prevention tools.

## Files:
- scan_results.txt: Nmap output
- Screenshots included
