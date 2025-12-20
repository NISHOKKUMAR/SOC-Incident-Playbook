# 📄 Phishing Incident Handling Report  
**Incident Type:** Malicious Email (Phishing with Malware Payload)  
**Prepared For:** SOC Analysts (Tier 1 / Tier 2)  
**Prepared By:** SOC Team  
**Date of Analysis:** 09-Dec-2022  

---

## 1️⃣ Executive Summary

An incoming email claiming to be a **commercial purchase receipt** was identified as a **phishing email delivering a malware payload**.  
The message impersonates a legitimate university staff member and attempts to trick recipients into downloading a malicious executable (`.exe`) disguised as an invoice.

The email was successfully detected by email security controls but requires analyst validation, containment, and IOC extraction.

---

## 2️⃣ Incident Metadata

| Field | Value |
|-----|------|
| Incident ID | PHISH-194 |
| Delivery Method | Email |
| Sender Display Name | ERIKA JOHANA LOPEZ VALIENTE |
| Sender Email | erikajohana.lopez@uptc.edu.co |
| Recipient | servicios.informaticos@fsfb.org.co |
| Subject | COMMERCIAL PURCHASE RECEIPT ONLINE 27 NOV |
| Malware Type | Spyware |
| Severity | **High** |
| User Interaction Required | Yes (Click + Download) |

---

## 3️⃣ Initial Detection

The email was flagged due to:
- Suspicious **invoice-related lure**
- External executable file download
- Mismatch between sender domain and email routing behavior
- Suspicious IP address hosting payload

The **email body contains a direct link to an `.exe` file**, which is a strong phishing indicator.

---

## 4️⃣ Email Header Analysis

### 4.1 Authentication Results

| Control | Result | Notes |
|------|------|------|
| SPF | SoftFail | Sending IP not authorized |
| DKIM | Fail | No valid DKIM signature |
| DMARC | None | No policy enforcement |
| ARC | Fail | Chain integrity failed |

🔴 **Conclusion:** Sender authentication cannot be trusted.

---

### 4.2 Sending Infrastructure

| Element | Value |
|------|------|
| Originating Mail Server | mail-wr1-f65.google.com |
| Payload Hosting IP | `107.175.247.199` |
| Country | United States |
| Email Gateway | Trend Micro |

🔴 Payload hosted on **raw IP address**, not a domain → **high-risk indicator**

---

## 5️⃣ Email Body & Content Analysis

### 5.1 Social Engineering Techniques Used

- Fake **purchase confirmation**
- Financial urgency ($625,000 pesos)
- Trust abuse using **real academic identity**
- Confidentiality notice to discourage verification
- Generic wording sent to **undisclosed recipients**

---

### 5.2 Malicious Indicators in Content

| Indicator | Description |
|--------|------------|
| File Type | `.exe` (Executable) |
| Delivery Method | Direct HTTP download |
| Disguised As | Invoice document |
| Link | `http://107.175.247.199/loader/install.exe` |
| Access Code | Fake legitimacy tactic |

🚨 **Invoices are never delivered as executable files**

---

## 6️⃣ Malware Risk Assessment

| Factor | Risk |
|----|----|
| Executable Payload | High |
| No HTTPS | High |
| IP-based Hosting | High |
| Financial Lure | Medium |
| Impersonation | High |

🟥 **Overall Risk Level: HIGH**

---

## 7️⃣ Indicators of Compromise (IOCs)

The following IOCs were extracted directly from the analyzed email and should be added to **SIEM, EDR, Email Gateway, and Network Security controls**.

---

### 7.1 Malicious URLs

| Type | Value | Description |
|----|------|------------|
| URL | `http://107.175.247.199/loader/install.exe` | Direct malware payload download masquerading as invoice |
| Defang URL | hxxp[://]107[.]175[.]247[.]199/loader/install[.]exe  |
---

### 7.2 Malicious IP Addresses

| IP Address | Role | Notes |
|-----------|------|------|
| 107.175.247.199 | Malware Hosting Server | Hosts executable payload |
| 18.208.22.104 | Email Relay (Suspicious) | SPF softfail observed |
| 209.85.221.65 | Gmail Relay | Legitimate but abused for delivery |

---

### 7.3 Email Addresses

| Type | Value |
|----|------|
| Sender Address | erikajohana.lopez@uptc.edu.co |
| Return-Path | erikajohana.lopez@uptc.edu.co |

⚠️ Likely **compromised or spoofed** legitimate account.

---

### 7.4 Domains

| Domain | Context |
|------|--------|
| uptc.edu.co | Impersonated sender domain |
| fsfb.org.co | Targeted recipient domain |

---

### 7.5 File Indicators

| Indicator | Value |
|--------|------|
| File Name | install.exe |
| File Type | Windows Executable |
| Delivery Method | HTTP download |
| Disguised As | Invoice document |
| Execution Requirement | User interaction |

---

### 7.6 Email Metadata Indicators

| Field | Value |
|----|------|
| Subject | COMMERCIAL PURCHASE RECEIPT ONLINE 27 NOV |
| Message-ID | `<CABWu4iua5_uex6=G8pi_OJz1tBLJiNakMK-1=7128orpzxbKxw@mail.gmail.com>` |
| Attachment | None (link-based delivery) |

---

### 7.7 Hashes

| Type | Value |
|----|------|
| File Hash | Not Available |
| Reason | Payload not downloaded during analysis |

📌 **Action:** If payload is retrieved in a sandbox, calculate:
- MD5
- SHA1
- SHA256

---

### 7.8 Network Patterns (Behavioral IOCs)

- HTTP download of executable over port 80
- IP-based hosting (no domain)
- No TLS encryption
- Direct user-click execution

---

## 8️⃣ SOC Incident Response Actions

- Block IP `107.175.247.199` at firewall
- Block URL at proxy and email gateway
- Monitor logs for access to `/loader/install.exe`
- Hunt for `install.exe` execution across endpoints
- Add sender address to watchlist or block it

---

##  9️⃣ Final Classification

> **Confirmed Phishing Email with Malware Delivery Attempt**

**MITRE ATT&CK Techniques:**
- T1566.001 – Phishing via Email
- T1204.002 – User Execution: Malicious File

## 📌 SOC Analyst Checklist (Quick Reference)

- [ ] Analyze headers (SPF/DKIM/DMARC)
- [ ] Extract and block IOCs
- [ ] Assess user interaction
- [ ] Contain and remediate
- [ ] Document findings
- [ ] Close incident

---

**Status:** Closed  
**Confidence Level:** High  

## 📎 Resource

The original phishing email used for this investigation is available below:

- **View Phishing Email (EML):**  
 [PHISH-194.eml](../resource/PHISH-194.eml?raw=true)

> This file contains full email headers and body content for your practice.