# 🔐 Cybersecurity Task 1: Port Scanning with Nmap

## 📌 Objective

The objective of this task is to perform a basic port scan on an authorized local system using Nmap. The purpose is to identify open TCP ports, determine the services associated with them, and understand potential network security risks.

## 🛠️ Tools Used

* **Windows 10**
* **Command Prompt (CMD)**
* **Nmap 7.97**

## 🌐 Network Information

* **Target IP:** `192.168.1.39`
* **Subnet Mask:** `255.255.255.0`
* **Local Network Range:** `192.168.1.0/24`

## ⚙️ Nmap Scan

### Scan Target

```text
192.168.1.39
```

### Scan Profile

```text
Intense Scan
```

### Command Used

```bash
nmap -sS 192.168.1.39
```

The `-sS` option performs a TCP SYN scan to identify open TCP ports on the target host.

## 📊 Scan Summary

The Nmap scan identified:

* **1 host online**
* **5 open TCP ports**
* **995 closed TCP ports**

### Open Ports

|    Port | State | Service        |
| ------: | ----- | -------------- |
| 135/tcp | Open  | msrpc          |
| 139/tcp | Open  | netbios-ssn    |
| 445/tcp | Open  | microsoft-ds   |
| 902/tcp | Open  | iss-realsecure |
| 912/tcp | Open  | apex-mesh      |

## 📄 Nmap Output

```text
Starting Nmap 7.97
Nmap scan report for 192.168.1.39
Host is up (0.00089s latency).
Not shown: 995 closed tcp ports (reset)

PORT    STATE SERVICE
135/tcp open  msrpc
139/tcp open  netbios-ssn
445/tcp open  microsoft-ds
902/tcp open  iss-realsecure
912/tcp open  apex-mesh

Nmap done: 1 IP address (1 host up) scanned in 0.76 seconds
```

## ⚠️ Security Risks & Observations

### Port 135 – MSRPC

Microsoft RPC services commonly use port 135. Although required by some Windows functionality, unnecessary exposure can increase the attack surface.

**Mitigation:**

* Restrict access using Windows Firewall.
* Allow RPC traffic only from trusted networks where required.

### Port 139 – NetBIOS

Port 139 is associated with NetBIOS Session Service and legacy Windows networking.

**Mitigation:**

* Disable NetBIOS over TCP/IP if it is not required.
* Restrict access to trusted networks.

### Port 445 – SMB

Port 445 is commonly used by Windows SMB for file and printer sharing.

**Mitigation:**

* Keep Windows fully updated.
* Enable Windows Firewall.
* Disable file sharing when it is not required.
* Restrict SMB access to trusted networks.

### Ports 902 and 912

Nmap identified these ports with the service names `iss-realsecure` and `apex-mesh`. Nmap service names are not always definitive, so the applications/processes using these ports should be verified on the target system.

**Mitigation:**

* Identify the application using each port.
* Disable unnecessary services.
* Restrict access using firewall rules when appropriate.

## 🛡️ General Recommendations

* Keep Windows and installed applications updated.
* Use Windows Firewall to restrict unnecessary inbound connections.
* Disable unused services.
* Regularly check for unexpected open ports.
* Use secure authentication mechanisms.
* Restrict network services to trusted networks.

## 📁 Project Files

```text
CyberSecurity-TASK-1/
│
├── README.md
│
├── Scan-Results/
│   └── scan_results.txt
│
└── Screenshots/
    ├── nmap-command.png
    └── scan-results.png
```

## 📸 Evidence

Screenshots showing the Nmap command and scan results should be included in the `Screenshots` folder.

The complete Nmap output is saved in:

```text
Scan-Results/scan_results.txt
```

## 🎓 Learning Outcome

Through this task, I gained practical experience in:

* Network reconnaissance
* TCP SYN scanning
* Nmap
* Identifying open ports
* Understanding network services
* Basic vulnerability and risk assessment
* Network security hardening
* Security documentation

## ⚠️ Disclaimer

This scan was performed on an authorized local system/network for educational and cybersecurity testing purposes. Nmap should only be used against systems and networks for which proper authorization has been obtained.

---

### 👨‍💻 Author

**Kunal Kumar**

Cybersecurity Learning Project
