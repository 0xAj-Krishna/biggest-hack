# VMware vCenter DCERPC RCE (CVE-2024-37079, CVE-2024-37080)

**CVE:** CVE-2024-37079, CVE-2024-37080  
**CWE:** CWE-122 (Heap-Based Buffer Overflow)  
**CVSS:** 9.8 (Critical)  

---

## 📝 What happened
In mid-2024, VMware disclosed two critical **heap overflow vulnerabilities** in the **DCERPC service** of vCenter Server.  
An attacker with network access could exploit these flaws to execute arbitrary code on the vCenter system.  
Because vCenter is the central management server for VMware ESXi hosts and virtual machines, a compromise here meant attackers could take control of entire data centers.  

---

## 💥 Impact
- Complete compromise of VMware environments through vCenter.  
- Attackers gained access to **all VMs, hosts, and data** managed by vCenter.  
- Data centers and enterprises running VMware were immediately at risk.  

---

## 🔑 Lesson learned
- Centralized management systems like vCenter are **high-value targets**.  
- Buffer overflows in critical services can lead to catastrophic compromise.  
- Isolating management networks reduces attack surface.  

---

## 🛡️ Mitigation / Recommendation
- Apply VMware’s patches immediately.  
- Restrict vCenter access to trusted management networks only.  
- Monitor for unusual activity in vCenter and ESXi logs.  
- Implement network segmentation for virtualization infrastructure.  

---

## 🔗 Sources
- [NVD – CVE-2024-37079](https://nvd.nist.gov/vuln/detail/CVE-2024-37079)  
- [VMware Advisory](https://www.vmware.com/security/advisories.html)  
- [CISA KEV Catalog](https://www.cisa.gov/known-exploited-vulnerabilities-catalog)  
