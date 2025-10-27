# 🧩 Alert Triage With Splunk  
**TryHackMe – Linux System Investigation**

### 🎯 Objective  
Investigate a brute-force SSH attack using Splunk and determine if the alert represents a true compromise.

---

### 🧠 Scenario  
- **Alert:** Brute Force Activity Detection  
- **Date:** 17/09/2025 09:00:21  
- **Target Host:** `tryhackme-2404`  
- **Source IP:** `10.10.242.248`  
- **Index:** `linux-alert`

---

### 🔍 Investigation Summary  
1. Queried Splunk logs for failed and accepted SSH login attempts.  
2. Detected multiple failed logins and invalid user attempts from the same IP.  
3. Identified 500+ failed attempts targeting `john.smith`.  
4. Confirmed a successful login → attacker gained access.  
5. Discovered privilege escalation to `root` and persistence account `system-utm`.

---

### 📊 Key Findings  
| Indicator | Result |
|------------|---------|
| Failed Attempts | 500 |
| Attack Duration | 5 minutes |
| Compromised User | john.smith |
| Privilege Escalation | root |
| Persistence User | system-utm |

---

### 🚨 Outcome  
Classified as **True Positive** — attacker successfully brute-forced the system and established persistence.  
Incident escalated to SOC Level 2 / Incident Response team.

---

### 🧰 Tools Used  
- **Splunk SIEM**  
- **Linux SSH Auth Logs (`/var/log/secure`)**

---

### 📚 Tags  
`#TryHackMe` `#Splunk` `#SOC` `#Linux` `#CyberSecurity` `#BruteForce` `#AlertTriage`
