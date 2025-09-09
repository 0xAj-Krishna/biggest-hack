# MOVEit Transfer SQL Injection (CVE-2023-34362)

**CVE:** CVE-2023-34362  
**CWE:** CWE-89 (SQL Injection)  
**CVSS:** 9.8 (Critical)  

---

## 📝 What happened
In May 2023, a **SQL injection vulnerability** was discovered in Progress Software’s **MOVEit Transfer** file transfer application.  
Attackers exploited the flaw to execute arbitrary SQL queries against the application’s database.  
This enabled them to upload **webshells** and steal sensitive files from organizations using MOVEit.  
The attack was carried out in large-scale campaigns, with automation used to hit hundreds of exposed servers at once.  

---

## 💥 Impact
- Hundreds of organizations worldwide were compromised.  
- Sensitive financial, government, and healthcare data was stolen.  
- MOVEit became one of the most widely exploited enterprise vulnerabilities of 2023.  

---

## 🔑 Lesson learned
- SQL injection is still one of the most devastating web application flaws.  
- File transfer applications are prime targets for data theft.  
- Mass exploitation can occur within hours of disclosure.  

---

## 🛡️ Mitigation / Recommendation
- Apply Progress Software’s security updates immediately.  
- Restrict public access to MOVEit Transfer servers.  
- Monitor logs for signs of exploitation (webshell uploads, abnormal queries).  
- Regularly test web apps for SQLi vulnerabilities using security tools.  

---

## 🔗 Sources
- [NVD – CVE-2023-34362](https://nvd.nist.gov/vuln/detail/CVE-2023-34362)  
- [Progress Software Advisory](https://www.progress.com/security)  
- [Microsoft Threat Intelligence Blog](https://www.microsoft.com/security/blog/)  
