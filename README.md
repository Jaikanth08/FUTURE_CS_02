# 🛡️ FUTURE_CS_02

## 📌 Task 2 – SOC Alert Monitoring & Incident Response

This repository contains my submission for **Task 2** of the **Cyber Security Internship** offered by **Future Interns**.

The task focused on simulating real-world SOC alert analysis using **Splunk** and identifying various types of security incidents such as malware infections, brute-force login attempts, and suspicious connections.

---

## 🧰 Tools Used

- 💻 Kali Linux (Virtual Machine)
- 🔍 Splunk Enterprise (Local Installation)
- 📄 Log File: `SOC_Task2_Sample_Logs.txt`
- 📷 Screenshot Tools (to capture query results)

---

## 🔍 Splunk Search Queries Used

```spl
# 1. Malware & Threat Detections
source="SOC_Task2_Sample_Logs.txt" (malware OR "Trojan Detected" OR "Rootkit Signature" OR "Spyware Alert" OR "Worm Infection Attempt" OR "Ransomware Behavior")

# 2. Login Failures / Authentication Issues
source="SOC_Task2_Sample_Logs.txt" ("login failed" OR "Failed login" OR "Failed password" OR "authentication failure")

# 3. Suspicious Connection Attempts
source="SOC_Task2_Sample_Logs.txt" "connection attempt" OR "unauthorized connection"

## 🧪 Incident Summary Table

| Alert Type             | User    | IP Address      | Time                | Description                           |
|------------------------|---------|------------------|---------------------|----------------------------------------|
| Malware Detected       | bob     | 10.0.0.5         | 2025-07-03 05:48:14 | Trojan activity detected               |
| Login Failure          | alice   | 203.0.113.77     | 2025-07-03 07:02:14 | Multiple failed login attempts         |
| Suspicious Connection  | david   | 203.0.113.77     | 2025-07-03 06:10:14 | Repeated unauthorized connection       |
| Rootkit Signature      | eve     | 10.0.0.5         | 2025-07-03 07:51:14 | Rootkit signature found on host        |

##📄 Report
#📁 Task_2_Incident_Response_Report.docx
The professional report includes:

Executive Summary

Toolchain Used

Splunk Queries

Screenshots ([img] placeholders)

Detected Alerts

Recommendations

Conclusion

##✅ Recommendations
Isolate affected systems showing malware behavior

Enforce Multi-Factor Authentication (MFA)

Apply firewall rules to block repeated failed login attempts

Monitor suspicious IPs and connection patterns

Regularly patch systems and update antivirus tools

##🎯 Outcome
Through this task, I learned how to:

Use Splunk as a SIEM tool for real-time log analysis

Identify and classify threats based on log patterns

Document and present security incidents professionally

Simulate a real-world SOC analyst workflow
# 4. User Behavior Summary
source="SOC_Task2_Sample_Logs.txt" | stats count by user
