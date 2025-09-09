# Progress WS_FTP Server RCE (CVE-2023-40044)

**CVE:** CVE-2023-40044  
**CWE:** CWE-502 (Deserialization of Untrusted Data)  
**CVSS:** 10.0 (Critical)  

---

## 📝 What happened
In September 2023, a critical vulnerability was found in **Progress WS_FTP Server**, a widely used file transfer application.  
The flaw was caused by unsafe **.NET deserialization**, which allowed attackers to send malicious objects that were executed on the server.  
This gave unauthenticated attackers the ability to run arbitrary commands remotely.  
Within days of disclosure, ransomware operators began mass exploitation campaigns.  

---

## 💥 Impact
- Enabled remote takeover of WS_FTP servers without authentication.  
- Ransomware and data theft campaigns quickly weaponized the bug.  
- Affected enterprises across finance, healthcare, and government sectors.  

---

## 🔑 Lesson learned
- Deserialization flaws can be as dangerous as SQL injection or buffer overflows.  
- File transfer servers are common ransomware targets.  
- Enterprises must prioritize patching of internet-facing file services.  

---

## 🛡️ Mitigation / Recommendation
- Upgrade WS_FTP to the patched version immediately.  
- Restrict external exposure of WS_FTP to trusted networks.  
- Monitor logs for suspicious uploads or command execution attempts.  
- Segment file transfer servers from critical infrastructure.  

---

## 🔗 Sources
- [NVD – CVE-2023-40044](https://nvd.nist.gov/vuln/detail/CVE-2023-40044)  
- [Progress Software Advisory](https://www.progress.com/security)  
- [Rapid7 Analysis](https://www.rapid7.com/blog/)  
