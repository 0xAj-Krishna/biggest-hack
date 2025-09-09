# GitLab Password Reset Account Takeover (CVE-2023-7028)

**CVE:** CVE-2023-7028  
**CWE:** CWE-306 (Missing Authentication), CWE-20 (Improper Input Validation)  
**CVSS:** 10.0 (Critical)  

---

## 📝 What happened
In January 2024, GitLab disclosed a severe vulnerability in its **password reset feature**.  
Due to a logic flaw, password reset emails could be sent to **unverified attacker-controlled addresses** instead of the legitimate account owner.  
This allowed attackers to **take over any GitLab account**, including administrator accounts with access to source code, CI/CD pipelines, and sensitive credentials.  
Because GitLab is widely used for software development, the consequences of account takeover were massive.  

---

## 💥 Impact
- Attackers could hijack developer and admin accounts.  
- Source code repositories and secrets exposed.  
- CI/CD pipelines at risk of supply-chain compromise.  

---

## 🔑 Lesson learned
- Account recovery mechanisms must be as secure as login mechanisms.  
- Logic flaws can be just as dangerous as code execution bugs.  
- Source code management platforms are high-value attack targets.  

---

## 🛡️ Mitigation / Recommendation
- Update GitLab instances to patched versions immediately.  
- Enforce multi-factor authentication on all accounts.  
- Monitor for suspicious password reset requests.  
- Audit repository logs for unusual access or commits.  

---

## 🔗 Sources
- [NVD – CVE-2023-7028](https://nvd.nist.gov/vuln/detail/CVE-2023-7028)  
- [GitLab Advisory](https://about.gitlab.com/releases/categories/releases/)  
- [CISA KEV Catalog](https://www.cisa.gov/known-exploited-vulnerabilities-catalog)  
