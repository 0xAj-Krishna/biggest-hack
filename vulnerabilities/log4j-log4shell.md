# Apache Log4j Log4Shell (CVE-2021-44228)

**CVE:** CVE-2021-44228  
**CWE:** CWE-74 (Improper Neutralization of Special Elements in Output)  
**CVSS:** 10.0 (Critical)  

---

## 📝 What happened
In December 2021, one of the most infamous vulnerabilities in history — **Log4Shell** — was disclosed.  
The flaw was in **Apache Log4j**, a popular Java logging library.  
A specially crafted log string could trigger a **JNDI lookup**, causing the application to fetch and execute remote code from an attacker-controlled server.  
Because Log4j is embedded in countless applications, from Minecraft servers to enterprise systems, exploitation spread globally within hours of disclosure.  

---

## 💥 Impact
- Millions of applications and servers were vulnerable.  
- Exploited for ransomware, crypto-mining, and botnet infections.  
- Forced emergency patching across the internet and cost billions in mitigation.  

---

## 🔑 Lesson learned
- Even small libraries can create **global risk** when widely used.  
- Dependency management and software composition analysis are vital.  
- Defense-in-depth is needed to limit the blast radius of zero-days.  

---

## 🛡️ Mitigation / Recommendation
- Upgrade to patched Log4j versions (2.17.1+).  
- Use web application firewalls (WAFs) to block JNDI exploit strings.  
- Monitor logs for exploitation attempts.  
- Reduce reliance on third-party libraries without proper security review.  

---

## 🔗 Sources
- [NVD – CVE-2021-44228](https://nvd.nist.gov/vuln/detail/CVE-2021-44228)  
- [Apache Log4j Advisory](https://logging.apache.org/log4j/2.x/security.html)  
- [Cloudflare Blog – Log4Shell](https://blog.cloudflare.com/inside-the-log4j2-vulnerability-cve-2021-44228/)  
