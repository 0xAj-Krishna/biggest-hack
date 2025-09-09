# F5 BIG-IP Unauth RCE (CVE-2023-46747, CVE-2023-46748)

**CVE:** CVE-2023-46747, CVE-2023-46748  
**CWE:** CWE-306 (Missing Authentication), CWE-20 (Improper Input Validation)  
**CVSS:** 9.8 (Critical)  

---

## 📝 What happened
In late 2023, critical vulnerabilities were discovered in **F5 BIG-IP**, a popular load balancer and firewall appliance.  
The flaws allowed **unauthenticated remote code execution** on the management interface.  
Attackers quickly weaponized the bugs, scanning the internet for exposed BIG-IP devices and compromising them en masse.  
Because BIG-IP devices often sit at the edge of enterprise networks, exploitation gave attackers a direct path inside.  

---

## 💥 Impact
- Attackers gained full control of BIG-IP appliances without logging in.  
- Widespread exploitation observed within days of disclosure.  
- Enabled theft of sensitive configs and credentials.  

---

## 🔑 Lesson learned
- Management interfaces should **never be exposed to the public internet**.  
- Appliances that secure networks are high-value targets.  
- Rapid patching is essential to prevent mass exploitation.  

---

## 🛡️ Mitigation / Recommendation
- Apply F5’s patched versions immediately.  
- Remove public exposure of the BIG-IP management interface.  
- Monitor devices for unauthorized changes.  
- Restrict access to management plane to internal networks only.  

---

## 🔗 Sources
- [NVD – CVE-2023-46747](https://nvd.nist.gov/vuln/detail/CVE-2023-46747)  
- [F5 Security Advisory](https://my.f5.com/manage/s/article/K000137353)  
- [CISA KEV Catalog](https://www.cisa.gov/known-exploited-vulnerabilities-catalog)  
