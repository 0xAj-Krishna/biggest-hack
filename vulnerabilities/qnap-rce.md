# QNAP QTS/QuTS Hero RCE (CVE-2023-23368)

**CVE:** CVE-2023-23368  
**CWE:** CWE-78 (OS Command Injection)  
**CVSS:** 9.8 (Critical)  

---

## 📝 What happened
In 2023, QNAP disclosed a **command injection vulnerability** in its **QTS and QuTS Hero** NAS operating systems.  
The flaw existed in the web management interface, where unsanitized input allowed attackers to execute arbitrary system commands.  
Hackers exploited the bug to install **crypto-mining malware** and steal data from vulnerable NAS devices exposed to the internet.  

---

## 💥 Impact
- Thousands of QNAP devices compromised worldwide.  
- Attackers installed miners and backdoors for persistence.  
- Home users and enterprises lost sensitive files.  

---

## 🔑 Lesson learned
- NAS devices are attractive to attackers due to internet exposure.  
- Web management interfaces must validate inputs properly.  
- Home and SMB networks are often part of larger attack campaigns.  

---

## 🛡️ Mitigation / Recommendation
- Apply QNAP’s patched firmware immediately.  
- Disable public internet access to NAS devices.  
- Back up data securely and offline.  
- Monitor for unauthorized processes or files on QNAP systems.  

---

## 🔗 Sources
- [NVD – CVE-2023-23368](https://nvd.nist.gov/vuln/detail/CVE-2023-23368)  
- [QNAP Advisory](https://www.qnap.com/en/security-advisory)  
- [The Hacker News Coverage](https://thehackernews.com/)  
