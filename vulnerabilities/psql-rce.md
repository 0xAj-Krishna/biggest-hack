# CVE-2025-1094 – PostgreSQL psql SQL Injection Vulnerability

## 📌 Overview
- **CVE ID:** CVE-2025-1094  
- **Product:** PostgreSQL (psql command-line tool)  
- **Type:** SQL Injection  
- **Severity:** High (CVSS score ~8)  
- **Date Published:** February 2025  
- **Affected Versions:**  
  - PostgreSQL < 17.3  
  - PostgreSQL < 16.7  
  - PostgreSQL < 15.11  
  - PostgreSQL < 14.16  
  - PostgreSQL < 13.19  
- **Fixed Versions:** PostgreSQL 17.3, 16.7, 15.11, 14.16, 13.19  

---

## 🧐 What is psql?
- `psql` is the **interactive command-line tool** bundled with PostgreSQL.  
- It allows users to:
  - Run SQL queries directly.  
  - Manage databases.  
  - Automate queries/scripts.  
- Widely used in enterprises, government systems, and cloud providers.  

---

## 🛠️ Vulnerability Details
- The flaw exists in **psql’s string escaping logic**.  
- PostgreSQL assumed escaping unsafe input = safe queries.  
- But **invalid UTF-8 byte sequences** broke this assumption:  
  - Malformed characters bypassed escaping.  
  - These slipped directly into SQL queries.  
  - Attacker could take control of query execution.  

---

## ⚡ Attack Vector
1. Attacker injects **malicious input with invalid UTF-8 characters**.  
2. Application/script passes this input into `psql`.  
3. Escaping fails → input injected into SQL query.  
4. Attacker executes arbitrary SQL commands.  

### Example
```sql
-- Expected safe query
SELECT * FROM users WHERE name = 'Alice';

-- Malicious input bypasses escaping
SELECT * FROM users WHERE name = 'Alice' OR '1'='1';
```

## 🎯 Impact

| **Impact Type**        | **Description** |
|-------------------------|-----------------|
| **Data Breach**        | Attackers can read, modify, or delete sensitive records. |
| **Authentication Bypass** | Malicious queries can bypass login checks. |
| **Privilege Escalation** | If the DB user has elevated rights, attacker may gain full database control. |
| **Remote Code Execution (RCE)** | Through psql meta-commands (`!ls`, `!cat /etc/passwd`) attackers can execute OS-level commands. |
| **Supply Chain Risk**  | CI/CD pipelines, backup scripts, and automation tools using psql could be compromised. |

---

## 🛡️ Remediation
- **Upgrade immediately** to patched versions:  
  - PostgreSQL 17.3, 16.7, 15.11, 14.16, 13.19  
- **Best Practices:**  
  - Use **parameterized queries** instead of manual escaping.  
  - Validate and normalize input (accept only valid UTF-8).  
  - Apply the **principle of least privilege** for database accounts.  
  - Monitor database logs for unusual queries or meta-command usage.  
  - Secure automation pipelines and CI/CD systems that invoke `psql`.  

---

## 📖 References
- [PostgreSQL Security Advisories](https://www.postgresql.org/support/security/)  
- [Rapid7 Blog – CVE-2025-1094](https://www.rapid7.com/blog/post/2025/02/13/cve-2025-1094-postgresql-psql-sql-injection-fixed/)  
- [OWASP Top 10 – Injection](https://owasp.org/Top10/A03_2021-Injection/)  

