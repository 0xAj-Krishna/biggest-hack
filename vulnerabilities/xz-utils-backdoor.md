# XZ Utils Supply-chain Backdoor (CVE-2024-3094)

**CVE:** CVE-2024-3094  
**CWE:** CWE-506 (Embedded Malicious Code)  
**CVSS:** 10.0 (Critical)  

---

## 📝 What happened
In March 2024, a backdoor was discovered inside the **xz/liblzma compression library**, which is widely used in Linux distributions.  
This wasn’t a normal vulnerability — it was a **supply-chain compromise**. A malicious maintainer, who had gained trust in the project, slipped backdoored code into the release tarballs (v5.6.0–5.6.1).  
The injected code altered **OpenSSH (sshd)** authentication, allowing attackers to log in with specially crafted keys and gain **root access**.  
The attack was only discovered when a Debian developer noticed unusual **CPU spikes in sshd** and dug deeper.  

---

## 💥 Impact
- Could have enabled attackers to take over **millions of Linux servers**.  
- Risked compromise of **critical infrastructure, cloud services, and enterprises**.  
- Considered one of the most dangerous **open-source supply-chain attacks** in history.  

---

## 🔑 Lesson learned
- Supply-chain trust must never rely on a single maintainer.  
- Use **reproducible builds** to detect tampering.  
- Perform independent verification of release artifacts before distribution.  

---

## 🛡️ Mitigation / Recommendation
- Roll back to safe versions (5.4.x).  
- Rebuild systems from **trusted sources**.  
- Validate packages using **cryptographic signatures**.  
- Rotate SSH host keys and monitor unusual sshd activity.  

---

## 🔗 Sources
- [NVD – CVE-2024-3094](https://nvd.nist.gov/vuln/detail/CVE-2024-3094)  
- [Red Hat Advisory](https://access.redhat.com/security/vulnerabilities/RHSB-2024-001)  
- [Debian Security Advisory](https://lists.debian.org/debian-security-announce/2024/msg00053.html)  
- [Ars Technica Coverage](https://arstechnica.com/security/2024/03/xz-utils-backdoor-linux/)  