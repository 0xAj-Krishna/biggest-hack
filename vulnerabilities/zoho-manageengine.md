# Zoho ManageEngine ADSelfService RCE (CVE-2021-40539)

**CVE:** CVE-2021-40539  
**CWE:** CWE-502 (Deserialization of Untrusted Data)  
**CVSS:** 9.8 (Critical)  

---

## 📝 What happened
In September 2021, Zoho disclosed a critical **unauthenticated remote code execution** vulnerability in **ADSelfService Plus**, an identity management and single sign-on solution.  
The flaw was due to insecure handling of API requests, which led to **deserialization of untrusted data**.  
Attackers exploited the bug to drop **webshells**, steal credentials, and escalate privileges within corporate networks.  
The vulnerability was exploited by both ransomware gangs and state-sponsored groups in targeted campaigns.  

---

## 💥 Impact
- Full remote takeover of ADSelfService Plus servers.  
- Compromise of Active Directory accounts and corporate credentials.  
- Used in targeted attacks against critical industries.  

---

## 🔑 Lesson learned
- Identity management systems are **crown jewels** for attackers.  
- Deserialization vulnerabilities are still common and dangerous.  
- APIs must undergo strict input validation and security reviews.  

---

## 🛡️ Mitigation / Recommendation
- Upgrade ADSelfService Plus to patched versions immediately.  
- Restrict external exposure of identity services.  
- Audit logs for webshell activity and unusual login attempts.  
- Enforce MFA and strict privilege management.  

---

## 🔗 Sources
- [NVD – CVE-2021-40539](https://nvd.nist.gov/vuln/detail/CVE-2021-40539)  
- [Zoho Advisory](https://www.manageengine.com/products/self-service-password/advisory.html)  
- [CISA Advisory](https://www.cisa.gov/news-events/alerts/2021/09/16/zoho-manageengine-vulnerability)  
