# Fortinet FortiOS SSL-VPN Overflow (CVE-2023-27997)

**CVE:** CVE-2023-27997  
**CWE:** CWE-122 (Heap-Based Buffer Overflow)  
**CVSS:** 9.2 (Critical)  

---

## 📝 What happened
In June 2023, a critical **heap-based buffer overflow** vulnerability was disclosed in **Fortinet FortiOS SSL-VPN**.  
The flaw allowed remote attackers to execute arbitrary code **without authentication**.  
It was confirmed to be actively exploited by advanced persistent threat (APT) groups even before patches were available.  
Because SSL-VPNs are internet-facing, attackers could compromise networks remotely with no user interaction.  

---

## 💥 Impact
- Thousands of Fortinet VPN appliances exploited worldwide.  
- Provided stealthy remote access into corporate and government networks.  
- Exploited by state-sponsored attackers for espionage.  

---

## 🔑 Lesson learned
- VPN appliances are high-value entry points and must be patched first.  
- Zero-day exploitation of security appliances is increasingly common.  
- Buffer overflows in C/C++ code remain a major attack vector.  

---

## 🛡️ Mitigation / Recommendation
- Apply Fortinet’s patched versions immediately.  
- Restrict exposure of SSL-VPN to trusted IPs if possible.  
- Monitor for abnormal login attempts and persistence mechanisms.  
- Conduct forensic analysis if compromise is suspected.  

---

## 🔗 Sources
- [NVD – CVE-2023-27997](https://nvd.nist.gov/vuln/detail/CVE-2023-27997)  
- [Fortinet Security Advisory](https://www.fortiguard.com/psirt)  
- [CISA Advisory](https://www.cisa.gov/news-events/alerts)  
