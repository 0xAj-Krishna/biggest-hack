# Citrix Bleed – NetScaler ADC/Gateway (CVE-2023-4966)

**CVE:** CVE-2023-4966  
**CWE:** CWE-120 (Buffer Copy without Checking Size), CWE-522 (Insufficient Token Protection)  
**CVSS:** 9.4 (Critical)  

---

## 📝 What happened
In October 2023, researchers revealed a vulnerability nicknamed **“Citrix Bleed”** in Citrix NetScaler ADC and Gateway appliances.  
The flaw allowed attackers to steal **session tokens** from memory. These tokens act like “tickets” proving a user is authenticated.  
By stealing them, attackers could **impersonate valid users** without knowing their passwords or MFA codes.  
The bug was quickly weaponized by ransomware groups, who used stolen tokens to move inside networks.  

---

## 💥 Impact
- Stolen session tokens bypassed MFA completely.  
- Ransomware gangs used the bug in real-world attacks.  
- Hundreds of organizations compromised before patches were applied.  

---

## 🔑 Lesson learned
- Session tokens must be strongly protected in memory.  
- After patching, organizations must also **force logouts** to invalidate stolen tokens.  
- MFA is not foolproof if tokens themselves are exposed.  

---

## 🛡️ Mitigation / Recommendation
- Patch Citrix ADC/Gateway devices immediately.  
- Force logout of all active sessions after patching.  
- Monitor logs for unusual activity tied to hijacked sessions.  
- Limit exposure of management interfaces to trusted networks.  

---

## 🔗 Sources
- [NVD – CVE-2023-4966](https://nvd.nist.gov/vuln/detail/CVE-2023-4966)  
- [Citrix Advisory](https://www.citrix.com/blogs/)  
- [Huntress Labs – Citrix Bleed](https://www.huntress.com/blog/citrix-bleed)  
