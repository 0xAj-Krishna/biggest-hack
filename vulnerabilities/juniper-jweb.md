# Juniper J-Web Exploit Chain (CVE-2023-36844–48)

**CVE:** CVE-2023-36844, CVE-2023-36845, CVE-2023-36846, CVE-2023-36847, CVE-2023-36848  
**CWE:** CWE-22 (Path Traversal), CWE-434 (Unrestricted File Upload)  
**CVSS:** 8.8 (High)  

---

## 📝 What happened
In August 2023, researchers discovered a chain of vulnerabilities in the **J-Web interface** of Juniper firewalls.  
The bugs allowed attackers to perform **path traversal** and **arbitrary file uploads**, which could then be executed as code on the device.  
Even worse, the flaws were **pre-authentication**, meaning attackers didn’t need valid credentials.  
Exploitation in the wild showed attackers installing **webshells** for persistence and remote control of affected devices.  

---

## 💥 Impact
- Attackers could gain full control of Juniper firewalls.  
- Webshells provided long-term persistence and lateral movement inside networks.  
- Internet-exposed J-Web devices were mass exploited.  

---

## 🔑 Lesson learned
- Exposing device management interfaces directly to the internet is dangerous.  
- Pre-authentication flaws in security appliances are highly attractive to attackers.  
- Appliances must undergo strict security audits and code reviews.  

---

## 🛡️ Mitigation / Recommendation
- Apply Juniper’s patches immediately.  
- Disable J-Web interface exposure on the internet.  
- Monitor for signs of compromise, especially unexpected files or processes.  
- Restrict management access to internal networks only.  

---

## 🔗 Sources
- [NVD – CVE-2023-36844](https://nvd.nist.gov/vuln/detail/CVE-2023-36844)  
- [Juniper Security Advisory](https://supportportal.juniper.net/s/article/2023-08-Security-Bulletin-J-Web-Remote-Code-Execution-Vulnerabilities)  
- [Shadowserver Report](https://www.shadowserver.org/news/juniper-exploited/)  
