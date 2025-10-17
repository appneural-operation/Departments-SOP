#  SOP5: Data Backup & Recovery

### **Purpose**

To ensure that all critical company data is **securely backed up**, **recoverable**, and **protected from loss or corruption** due to system failures, cyber incidents, or disasters.
This SOP establishes standardized procedures for **data backup scheduling, verification, and disaster recovery** across APPNEURAL Pvt. Ltd.

---

### **Scope**

This SOP applies to:

* All company data stored on servers, cloud platforms, and employee systems.
* Business-critical applications, databases, project files, and HR/Finance records.
* All IT and system administrators responsible for data security and continuity.

---

### **Objectives**

* Maintain **data integrity** and **availability** at all times.
* Ensure **timely recovery** of data during system crashes or disasters.
* Minimize business downtime and data loss.
* Comply with legal and security standards (IT Act 2000, ISO 27001).

---

## 🧭 **Step-by-Step Workflow**

### **Step 1: Identification of Critical Data & Systems**

1. Classify all data into the following categories:

   * **Critical:** Financial data, project databases, client files, HR records.
   * **Important:** Team communication, marketing content, reports.
   * **Non-Critical:** Temporary files, cached data, testing files.
2. Maintain a **Data Classification Register** including:

   * Data owner (Department Head)
   * Storage location (server, cloud, device)
   * Backup type and frequency
3. Review data classification **quarterly** or after any major system change.

---

### **Step 2: Define Backup Strategy**

1. Choose backup methods based on system requirements:

   * **Full Backup:** Copies all data (done weekly).
   * **Incremental Backup:** Copies only changed files (done daily).
   * **Differential Backup:** Copies changes since the last full backup (mid-week).
2. Store backups in **two locations**:

   * **Primary Backup:** On-site NAS (Network Attached Storage).
   * **Secondary Backup:** Off-site cloud server (e.g., AWS S3, Google Cloud).
3. Encrypt all backup data using AES-256 encryption.
4. Apply **Multi-Factor Authentication (MFA)** for backup access.

---

### **Step 3: Schedule & Monitor Backups**

1. IT sets up **automated backup jobs** using tools like:

   * AWS Backup / Google Drive Sync / Azure Backup / Local NAS Scheduler.
2. Frequency:

   * **Daily incremental backups** at 11:00 PM.
   * **Weekly full backups** every Saturday night.
3. IT team reviews **backup logs daily** for errors or incomplete backups.
4. Any failed backup must be retried within **24 hours** and documented.

---

### **Step 4: Backup Verification & Testing**

1. Perform **monthly backup testing** to confirm data recoverability.
2. Randomly select files or databases and attempt to restore them in a sandbox environment.
3. Verify file integrity, access permissions, and timestamps.
4. Record test results in the **Backup Verification Log.**
5. Any discrepancies must be corrected immediately, and the issue logged in the **Incident Register.**

---

### **Step 5: Disaster Recovery Planning**

1. Develop a **Disaster Recovery Plan (DRP)** that includes:

   * System restoration sequence (which systems to restore first).
   * Designated recovery team and contact list.
   * Access to backup credentials and storage locations.
   * Maximum acceptable downtime (RTO) and data loss limit (RPO).
2. Store the DRP in both **digital and printed format**.
3. Conduct **bi-annual disaster recovery drills** to simulate real-life incidents.

---

### **Step 6: Data Restoration Procedure**

1. Upon system failure or data corruption:

   * Identify affected systems and determine last successful backup.
   * Restore data from the **most recent verified backup**.
   * Test restored data for integrity before resuming operations.
2. Document:

   * Root cause of data loss.
   * Recovery time taken.
   * Data restored successfully (Y/N).
3. Report findings to IT Manager and Operations Head.

---

### **Step 7: Retention & Archiving**

1. Retain backups as per company policy:

   * **Daily backups:** retained for 7 days.
   * **Weekly backups:** retained for 1 month.
   * **Monthly backups:** retained for 1 year.
   * **Annual backups:** retained for 5 years (legal compliance).
2. Archive old data in read-only format for audit purposes.
3. Securely delete obsolete backups using **certified data destruction tools.**

---

### **Step 8: Documentation & Audit**

1. Maintain the following records:

   * Backup Schedule Log
   * Backup Verification Log
   * Disaster Recovery Test Report
   * Incident Report Log
2. Conduct **quarterly internal audits** of backup and recovery processes.
3. Retain all records for **at least 3 years.**

---

## 🧾 **Roles & Responsibilities**

| **Role**             | **Responsibilities**                                              |
| -------------------- | ----------------------------------------------------------------- |
| **IT Administrator** | Manage backup configuration, schedule, and monitoring.            |
| **System Admin**     | Test backups and validate recovery integrity.                     |
| **Department Head**  | Identify critical data for backup inclusion.                      |
| **IT Manager**       | Oversee DRP, handle escalations, and approve recovery procedures. |
| **Operations Head**  | Review reports and ensure business continuity readiness.          |

---

## 📋 **Templates**

### **Template 1 – Data Classification Register**

| Data Type            | Department  | Storage Location   | Backup Type        | Frequency | Owner     | Last Reviewed |
| -------------------- | ----------- | ------------------ | ------------------ | --------- | --------- | ------------- |
| Client Project Files | Development | Cloud Server (AWS) | Full + Incremental | Daily     | Tech Lead | 01-Oct-2025   |

---

### **Template 2 – Backup Schedule Log**

| Date        | Backup Type | System/Folder | Status     | Verified By | Remarks       |
| ----------- | ----------- | ------------- | ---------- | ----------- | ------------- |
| 15-Oct-2025 | Full        | HR Drive      | Successful | IT Admin    | Verified – OK |

---

### **Template 3 – Backup Verification Log**

| Date        | System           | Test Type       | Restored Successfully | Verified By  | Comments        |
| ----------- | ---------------- | --------------- | --------------------- | ------------ | --------------- |
| 30-Sep-2025 | Finance Database | Partial Restore | ✅ Yes                 | System Admin | No errors found |

---

### **Template 4 – Disaster Recovery Test Report**

| Test Date   | Scenario     | Recovery Time (RTO) | Data Loss (RPO) | Outcome    | Corrective Action                         |
| ----------- | ------------ | ------------------- | --------------- | ---------- | ----------------------------------------- |
| 01-Jul-2025 | Server Crash | 2 hrs               | 15 mins         | Successful | Improve backup frequency for payroll data |

---

## 💡 **Best Practices**

* Store one backup **off-site or in the cloud** to avoid loss from physical damage.
* Use **3-2-1 backup rule**:

  * 3 copies of data
  * 2 different media types
  * 1 stored off-site
* Encrypt backups before transfer or cloud upload.
* Automate alerts for failed backups.
* Test backups regularly (at least monthly).
* Document every backup activity and maintain logs.

---

## 📈 **Key Performance Indicators (KPIs)**

* Backup success rate (Target: 100%)
* Backup verification success rate (Target: ≥95%)
* Average recovery time (Target: <4 hours)
* Data loss incidents per year (Target: 0)

---

## ⚖️ **Compliance & Legal Reference**

* **Information Technology Act, 2000 (India)** – mandates secure data storage and access control.
* **ISO/IEC 27001:2013** – international standard for information security management.
* **GDPR (if applicable)** – for client or partner data involving EU residents.

---
