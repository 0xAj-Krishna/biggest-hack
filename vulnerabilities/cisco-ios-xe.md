# Cisco IOS XE Web UI Implant (CVE-2023-20198, CVE-2023-20273)

**CVE:** CVE-2023-20198, CVE-2023-20273  
**CWE:** CWE-269 (Improper Privilege Management), CWE-77 (Command Injection)  
**CVSS:** 10.0 (Critical)  

---

## 📝 What happened
In late 2023, Cisco disclosed that attackers were actively exploiting two vulnerabilities in its **IOS XE software**, which runs on enterprise routers and switches.  
The first flaw (CVE-2023-20198) allowed attackers to create **rogue admin accounts** via the Web UI without authentication.  
The second flaw (CVE-2023-20273) enabled attackers to execute arbitrary commands, including installing a **persistent implant** that survived reboots.  
Thousands of Cisco devices directly exposed to the internet were hijacked, giving attackers remote control over critical networking gear.  

---

## 💥 Impact
- Tens of thousands of enterprise routers and switches compromised worldwide.  
- Attackers gained long-term persistence with implants that survived reboots.  
- Allowed remote control of backbone networking infrastructure.  

---

## 🔑 Lesson learned
- Never expose device Web UIs directly to the internet.  
- Critical infrastructure gear (routers, firewalls) is highly attractive to attackers.  
- Persistence implants in firmware are especially dangerous.  

---

## 🛡️ Mitigation / Recommendation
- Immediately disable the Web UI on Cisco IOS XE devices exposed to the internet.  
- Apply Cisco’s patched versions.  
- Audit for rogue accounts and suspicious implants.  
- Restrict management access to internal networks or VPN only.  

---

## 🔗 Sources
- [NVD – CVE-2023-20198](https://nvd.nist.gov/vuln/detail/CVE-2023-20198)  
- [Cisco Security Advisory](https://sec.cloudapps.cisco.com/security/center/publicationListing.x)  
- [Ars Technica – Cisco Implant](https://arstechnica.com/security/2023/10/cisco-ios-xe-hacked/)  
