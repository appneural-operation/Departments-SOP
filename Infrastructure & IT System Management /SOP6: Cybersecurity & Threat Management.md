# **SOP: Cybersecurity & Threat Management**

## 🧭 **Purpose**

To protect **APPNEURAL Pvt. Ltd.** from internal and external cybersecurity threats by implementing robust preventive, detective, and corrective controls.
This ensures **data confidentiality, system integrity, and operational continuity**, aligning with the **IT Act 2000 (India)**, **GDPR (if applicable)**, and global best security practices.

---

## 📘 **Scope**

This SOP applies to:

* All employees, interns, vendors, and contractors using APPNEURAL’s IT systems.
* All digital assets including **servers, laptops, applications, databases, networks, and cloud systems**.
* All data types — confidential, internal, and public.

---

## 👥 **Roles & Responsibilities**

| **Role**                 | **Responsibility**                                                                             |
| ------------------------ | ---------------------------------------------------------------------------------------------- |
| **IT Administrator**     | Implement, monitor, and maintain security infrastructure and tools.                            |
| **System Administrator** | Manage network security configurations, patches, and firewalls.                                |
| **All Employees**        | Adhere to cybersecurity policies, report suspicious activities, and maintain password hygiene. |
| **Department Heads**     | Ensure team compliance and approve security-related access.                                    |
| **Management / CISO**    | Review audit reports, approve updates to policies, and ensure organization-wide readiness.     |

---

## ⚙️ **Detailed Workflow (Step-by-Step Process)**

### **Step 1: Security Infrastructure Setup**

* Deploy **firewalls**, **antivirus**, and **endpoint protection** across all devices.
* Enable **real-time threat detection** and **automatic updates** for antivirus definitions.
* Restrict administrative access only to IT personnel.
* Configure **Intrusion Detection and Prevention Systems (IDS/IPS)** for network monitoring.
* Set up **email security filters** (anti-phishing, spam filters, attachment scanners).

---

### **Step 2: Threat Monitoring & Detection**

* Monitor system logs, network activity, and login attempts **24/7 using SIEM tools**.
* Generate **automated alerts** for unusual behavior (e.g., multiple login failures, large data downloads).
* Maintain **Security Log Register** for daily, weekly, and monthly reviews.
* Perform vulnerability scans monthly to identify outdated or weak systems.

---

### **Step 3: Incident Response Procedure**

* **Immediate Action:**

  * Isolate affected system(s) from the network.
  * Disable compromised user accounts.
  * Preserve logs for forensic analysis.
* **Incident Documentation:**

  * Log details in the *Cybersecurity Incident Report Template* (see below).
  * Record affected data/systems and suspected source.
* **Root Cause Analysis:**

  * Identify how the breach occurred (e.g., phishing, outdated patch, weak password).
  * Document corrective steps.
* **Post-Incident Recovery:**

  * Restore data using verified backups.
  * Run a complete malware scan before reconnecting systems.
  * Communicate updates to management and relevant departments.

---

### **Step 4: User Awareness & Training**

* Conduct **quarterly cybersecurity awareness sessions** for all staff.
* Topics to include:

  * Safe email practices and phishing identification
  * Password management
  * Social engineering awareness
  * Safe use of external devices (USBs, drives)
  * Data privacy and handling protocols
* Conduct **cyber drills** (e.g., simulated phishing tests) to measure employee awareness.

---

### **Step 5: Security Audits & Compliance**

* Conduct **internal audits quarterly** and **external audits annually**.
* Verify compliance with:

  * IT Act 2000
  * GDPR / ISO 27001 standards
  * Company IT Security Policy
* Maintain audit logs and records for a minimum of **7 years**.
* Implement corrective measures based on audit findings.

---

### **Step 6: Data Recovery & Business Continuity**

* Validate **backup and recovery plans** quarterly.
* Ensure critical systems can be restored within **4–8 hours (RTO)**.
* Store at least **one backup copy offsite or on secure cloud storage**.
* Test **disaster recovery drills** annually to evaluate readiness.

---

## 📊 **Performance Metrics (KPIs)**

| **Metric**                                      | **Target**     |
| ----------------------------------------------- | -------------- |
| % of systems with updated antivirus definitions | 100%           |
| Incident detection & response time              | Within 1 hour  |
| Employee training completion rate               | 100% quarterly |
| Audit compliance score                          | ≥ 90%          |
| Backup success rate                             | ≥ 99%          |

---

## 📋 **Templates**

### **1. Cybersecurity Incident Report Template**

| **Field**              | **Details**                                                |
| ---------------------- | ---------------------------------------------------------- |
| Incident ID            | CSIR/2025/___                                              |
| Date & Time Detected   |                                                            |
| Reported By            |                                                            |
| System/Asset Affected  |                                                            |
| Type of Threat         | (Phishing / Malware / Unauthorized Access / DDoS / Others) |
| Severity Level         | Low / Medium / High / Critical                             |
| Description            |                                                            |
| Immediate Action Taken |                                                            |
| Root Cause Identified  |                                                            |
| Data Loss (if any)     | Yes / No                                                   |
| Corrective Measures    |                                                            |
| Restored from Backup?  | Yes / No                                                   |
| Verified By            | IT Head                                                    |
| Closure Date           |                                                            |

---

### **2. Cybersecurity Awareness Training Log**

| **Employee Name** | **Department** | **Training Date** | **Topic Covered** | **Trainer Name** | **Status (Completed/Pending)** |
| ----------------- | -------------- | ----------------- | ----------------- | ---------------- | ------------------------------ |
|                   |                |                   |                   |                  |                                |

---

## 🔒 **Best Practices for Cybersecurity & Threat Management**

### **Best Practices**

1. **Use Multi-Factor Authentication (MFA)** for all critical systems and accounts.
2. **Encrypt all sensitive data** in storage and during transfer.
3. **Apply software updates and security patches** weekly or as released.
4. **Segment networks** — keep internal, guest, and development networks isolated.
5. Enable **secure VPN connections** for remote workers.
6. Implement **“Least Privilege” principle** — grant only the minimum necessary access.
7. **Disable unused ports/services** on all servers and devices.
8. Use **endpoint detection & response (EDR)** systems for real-time monitoring.
9. Regularly **rotate encryption keys and passwords** (every 90 days).
10. **Monitor third-party integrations** for vulnerabilities.

---

### **Operational Best Practices**

1. Maintain **cyber hygiene checklist** for daily/weekly IT maintenance.
2. Conduct **risk assessment** bi-annually to identify emerging threats.
3. Keep a **Cyber Crisis Response Team (CCRT)** with defined roles and escalation paths.
4. Ensure **vendor security assessments** before onboarding any new third-party provider.
5. Retain **logs and audit trails for at least 1 year** for forensic analysis.
6. Use **secure password managers** for storing credentials.
7. Implement **email authentication protocols** (SPF, DKIM, DMARC) to prevent spoofing.

---

### **Employee Awareness Best Practices**

1. Never share passwords or OTPs via chat/email.
2. Avoid clicking unknown links or downloading attachments from unverified sources.
3. Lock screens when away from the workstation.
4. Report **any suspicious emails, pop-ups, or system behavior immediately** to IT.
5. Do not install unapproved software or browser extensions.

---

## 🔁 **Review & Version Control**

| **Version** | **Date**      | **Changes Made**                | **Approved By** |
| ----------- | ------------- | ------------------------------- | --------------- |
| 1.0         | Oct 2025      | Initial SOP creation            | IT Head         |
| 1.1         | (Next Update) | Annual Review and Audit Updates | MD / CISO       |

---

