# Palo Alto PAN-OS GlobalProtect RCE (CVE-2024-3400)

**CVE:** CVE-2024-3400  
**CWE:** CWE-77 (Command Injection)  
**CVSS:** 10.0 (Critical)  

---

## 📝 What happened
In April 2024, a critical **remote code execution** vulnerability was discovered in the **GlobalProtect service** of Palo Alto Networks firewalls.  
Attackers could send specially crafted requests to the service and achieve **root-level code execution without any authentication**.  
Since GlobalProtect is exposed on internet-facing firewalls, thousands of organizations were at risk immediately.  
Within days of disclosure, multiple threat actors had automated exploitation to steal configurations, extract credentials, and install persistence.  

---

## 💥 Impact
- Firewalls, which are meant to **protect networks**, became initial entry points.  
- Attackers gained full root control over compromised appliances.  
- Sensitive data like VPN credentials and configurations were stolen.  

---

## 🔑 Lesson learned
- Security appliances themselves can become **prime targets**.  
- Patch firewalls and VPNs **before anything else** in your environment.  
- Defense-in-depth (WAF, segmentation) reduces exposure.  

---

## 🛡️ Mitigation / Recommendation
- Upgrade PAN-OS to the fixed version immediately.  
- Apply interim mitigations such as Palo Alto’s **Threat IDs**.  
- Restrict GlobalProtect exposure to trusted networks if possible.  
- Monitor for unusual firewall activity or unauthorized accounts.  

---

## 🔗 Sources
- [NVD – CVE-2024-3400](https://nvd.nist.gov/vuln/detail/CVE-2024-3400)  
- [Unit 42 Blog](https://unit42.paloaltonetworks.com/)  
- [CISA Known Exploited Vulnerabilities](https://www.cisa.gov/known-exploited-vulnerabilities-catalog)  
