# Honeypot EC2 Lab – Cowrie SSH Brute Force Simulation

This lab demonstrates how to deploy and test a Cowrie honeypot on an AWS EC2 instance, using Hydra from a Kali Linux machine to simulate SSH brute-force attacks.

## 🛠 Setup Overview

1. Launch EC2 with Cowrie on port 2222.
2. Configure firewall for controlled access.
3. Launch Kali Linux with Hydra.
4. Simulate brute force using `rockyou.txt`.
5. Capture logs from Cowrie session.

## 🔍 Key Details

- EC2 Public IP: `54.91.232.240`
- Cowrie port: `2222`
- Hydra wordlist: `/usr/share/wordlists/rockyou.txt`
- Logs found in `cowrie/log/cowrie.log`

## 📸 Screenshots

Screenshots are provided and named in order (01.png, 02.png, ...) in the `screenshots/` folder for easy GitHub rendering.

## ⏱ Brute Force Summary

- Hydra attempted over 14 million combinations.
- Attack timed out after initial attempts due to Cowrie handling.

## 📁 Structure

```
honeypot_ec2_lab_complete/
│
├── README.md
├── DISCLAIMER.md
└── screenshots/
    ├── 01.png
    ├── 02.png
    └── ...
```

## 🔐 Security Reminder

This project is for educational use only. Never run such configurations in a production environment or open internet without protection.
