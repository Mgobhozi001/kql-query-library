# 🔍 KQL Query Library

A growing collection of Kusto Query Language (KQL) queries for Microsoft Sentinel, built for threat detection, hunting, and incident investigation.

Each query is documented with its purpose, the data source it expects, and MITRE ATT&CK mapping where applicable.

---

## 📁 Structure

```
queries/
├── authentication/   # Sign-in anomalies, brute force, impossible travel
├── network/          # Suspicious network traffic, DNS, firewall
├── endpoint/         # Process execution, persistence, malware indicators
└── cloud/            # Azure resource changes, privilege escalation
```

---

## 🗂️ Query Index

| Query                                                                 | Category       | MITRE ATT&CK              | Data Source                  |
| ---------------------------------------------------------------------- | -------------- | -------------------------- | ----------------------------- |
| [Impossible Travel Detection](queries/authentication/impossible-travel.kql) | Authentication | T1078 – Valid Accounts      | SigninLogs                    |
| [Failed Sign-in Spike (Brute Force)](queries/authentication/failed-signin-spike.kql) | Authentication | T1110 – Brute Force         | SigninLogs                    |
| [Suspicious PowerShell Execution](queries/endpoint/suspicious-powershell.kql) | Endpoint       | T1059.001 – PowerShell      | DeviceProcessEvents           |
| [New Admin Role Assignment](queries/cloud/new-admin-role-assignment.kql) | Cloud          | T1098 – Account Manipulation | AuditLogs                     |
| [Rare External DNS Query Volume](queries/network/rare-external-dns.kql) | Network        | T1071.004 – DNS             | DnsEvents                     |

*(Table updated as new queries are added.)*

---

## 🎯 Purpose

This library exists as a practical, hands-on companion to my Microsoft security certifications (SC-200, SC-500) and my [Employment Phishing SOC Case Study](https://github.com/Mgobhozi001/Spearphishing-via-Job-Portal-Scraping-Employment-Lure-with-Identity-Harvesting-and-Document-Fraud-I). Rather than only studying detection theory, I'm building and testing real queries against the log tables analysts use daily in Microsoft Sentinel.

---

## 🛠️ How to Use

1. Copy the query from the relevant `.kql` file
2. Paste into **Microsoft Sentinel → Logs**
3. Adjust the time range and any environment-specific fields (table names, thresholds)
4. Save as an Analytics Rule if you want it to run continuously

---

## 📬 Connect

[GitHub](https://github.com/Mgobhozi001) | [LinkedIn](https://www.linkedin.com/in/sphamandla-mgobhozi-3804a9252/)
