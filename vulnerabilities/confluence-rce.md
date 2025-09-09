# Atlassian Confluence RCE/Admin Creation (CVE-2023-22518, CVE-2023-22515)

**CVE:** CVE-2023-22518, CVE-2023-22515  
**CWE:** CWE-306 (Missing Authentication), CWE-269 (Improper Privilege Management)  
**CVSS:** 10.0 (Critical)  

---

## 📝 What happened
Atlassian’s **Confluence Server** suffered two back-to-back critical vulnerabilities in 2023.  
- CVE-2023-22518 allowed **unauthenticated remote code execution** (RCE).  
- CVE-2023-22515 let attackers **create unauthorized administrator accounts**.  
Within days of disclosure, attackers mass-scanned the internet for vulnerable Confluence servers and exploited them to gain full control.  
Since Confluence often stores internal documentation and credentials, this posed a severe risk to enterprises.  

---

## 💥 Impact
- Thousands of Confluence servers compromised worldwide.  
- Attackers gained control of collaboration systems used daily inside companies.  
- Allowed theft of sensitive internal documentation and secrets.  

---

## 🔑 Lesson learned
- Collaboration tools like Confluence are attractive attack surfaces.  
- Exposing internal tools directly to the internet is risky.  
- Patching delays can result in **mass compromise within days**.  

---

## 🛡️ Mitigation / Recommendation
- Patch Confluence servers immediately to the latest version.  
- Monitor for unauthorized admin accounts.  
- Restrict Confluence access to VPN or SSO-protected environments.  
- Regularly back up Confluence data securely.  

---

## 🔗 Sources
- [NVD – CVE-2023-22518](https://nvd.nist.gov/vuln/detail/CVE-2023-22518)  
- [Atlassian Security Advisory](https://confluence.atlassian.com/security)  
- [CISA KEV Catalog](https://www.cisa.gov/known-exploited-vulnerabilities-catalog)  
