# ⚠️ Disclaimer

This project is intended **strictly for educational purposes only**.

The EternalBlue vulnerability (MS17-010) demonstrated in this lab is a known exploit that has been used in malicious attacks such as WannaCry. This lab environment is isolated and should only be conducted in a **controlled, non-production setting** like Oracle VirtualBox with internal networking.

## 🛡️ Ethical Notice
- Do **not** attempt to replicate this lab against unauthorized systems.
- Ensure you have **explicit permission** before performing any type of penetration testing.
- Misuse of this information can result in criminal charges.

## ✅ Mitigation Strategies

To protect systems against EternalBlue and similar vulnerabilities, follow these best practices:

### 1. **Apply Security Patches**
- Ensure Windows systems are fully updated with the latest security patches.
- Apply Microsoft’s patch for MS17-010 immediately.

### 2. **Disable SMBv1**
- Disable Server Message Block version 1 (SMBv1) protocol, which is outdated and insecure.
```powershell
Set-SmbServerConfiguration -EnableSMB1Protocol $false
```

### 3. **Use Network Segmentation**
- Isolate critical systems and services to reduce exposure.

### 4. **Deploy Firewalls and IDS/IPS**
- Block access to SMB ports (e.g., 445) from untrusted networks.
- Monitor for suspicious traffic with intrusion detection systems.

### 5. **Enable Automatic Updates**
- Enable Windows Update or use a centralized patch management solution.

### 6. **Backup Critical Data**
- Regularly back up important files and store backups offline to protect against ransomware.

---

By following these mitigation strategies and using labs responsibly, we contribute to a more secure cyber environment.

