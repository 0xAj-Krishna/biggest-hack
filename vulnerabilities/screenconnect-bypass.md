# ConnectWise ScreenConnect Auth Bypass (CVE-2024-1709, CVE-2024-1710)

**CVE:** CVE-2024-1709, CVE-2024-1710  
**CWE:** CWE-288 (Authentication Bypass), CWE-22 (Path Traversal)  
**CVSS:** 10.0 (Critical)  

---

## 📝 What happened
In February 2024, security researchers disclosed two critical flaws in **ConnectWise ScreenConnect**, a remote monitoring and management (RMM) tool used by IT service providers.  
- CVE-2024-1709 allowed **unauthenticated access** to the web interface.  
- CVE-2024-1710 was a **path traversal bug** that let attackers upload malicious files.  
Together, they allowed hackers to create fake admin accounts and push malware to all endpoints managed by the IT provider.  
Because ScreenConnect is widely used by Managed Service Providers (MSPs), exploitation meant attackers could compromise **multiple organizations at once**.  

---

## 💥 Impact
- Ransomware and malware campaigns spread through compromised MSPs.  
- Attackers gained remote access to thousands of client systems.  
- IT providers became a **force multiplier** for attackers.  

---

## 🔑 Lesson learned
- RMM tools are high-value targets since they control many networks.  
- Authentication and input validation are critical in remote access software.  
- Compromise of one IT provider can cascade into dozens of victims.  

---

## 🛡️ Mitigation / Recommendation
- Immediately upgrade to patched versions of ScreenConnect.  
- Disable external access to the management interface when possible.  
- Monitor for creation of unauthorized admin accounts.  
- Segment RMM tools from production networks.  

---

## 🔗 Sources
- [NVD – CVE-2024-1709](https://nvd.nist.gov/vuln/detail/CVE-2024-1709)  
- [ConnectWise Advisory](https://www.connectwise.com/company/trust/security-bulletins)  
- [Huntress Labs Analysis](https://www.huntress.com/blog)  
