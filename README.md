# Firewall-rules-on-windows
# 🔐 Task 4: Setup and Use a Firewall on Windows

## 🎯 Objective
Configure and test basic firewall rules to allow or block traffic on a system.

## 🧰 Tools Used
- **Attacker Machine**: Kali Linux (Nmap for scanning)
- **Target Machine**: Windows 7
- **Firewall**: Windows Firewall (GUI configuration)

---

## 📝 Task Summary

This project demonstrates how firewall rules can be used to block or allow specific network ports. The test involves scanning from Kali Linux to a Windows 7 machine before and after applying inbound rules.

---

## 🛠️ Step-by-Step Process

### 1. Listed Current Firewall Rules
- Initially, Windows Firewall was **disabled**.
- All ports were visible to external scans (verified using Nmap from Kali Linux).

### 2. Enabled Windows Firewall
- Once enabled, **all ports appeared filtered** in Nmap scans.
- This behavior shows Windows blocks all unsolicited traffic by default.

### 3. Blocked Inbound Traffic on Port 139
- Created a rule in Windows Firewall to **block TCP port 139**.
- This step was to simulate denying access to a specific service.

### 4. Verified Using Nmap
- With firewall **enabled**, all ports were already filtered, so no visible difference was seen after blocking.

### 5. Allowed Traffic on Port 139
- Created another rule to **allow TCP port 139**.
- This helped validate how exceptions to firewall rules can allow external communication.

### 6. Tested the Allowed Rule
- Ran Nmap from Kali targeting port 139:
- nmap -p 139 192.168.1.102
- Result: Port 139 was now visible as **open**.

### 7. Documentation
- Screenshots taken for:
- Before enabling firewall (all ports open)
- After enabling firewall (all ports filtered)
- After allowing specific port (port visible again)
- Firewall GUI rule screenshots also included.

---

## 📊 Observations

- Enabling the firewall alone blocks unsolicited traffic on all ports.
- Specific firewall rules are needed to allow traffic on desired ports.
- Without allowing a port explicitly, Nmap scans return ports as `filtered`.
- Adding a rule to allow the port (e.g., 139) makes it accessible externally.

---

## 📌 Conclusion

This project effectively demonstrates the practical impact of firewall rules on network visibility and control. It highlights how specific ports can be controlled through inbound rules, providing a foundation for understanding host-based security mechanisms.



