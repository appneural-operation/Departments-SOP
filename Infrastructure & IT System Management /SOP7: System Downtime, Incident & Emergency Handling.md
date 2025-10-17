# **SOP: System Downtime, Incident & Emergency Handling**

## **Purpose**

To ensure rapid response, minimal disruption, and effective recovery from system downtime, IT incidents, or emergencies. This SOP establishes a structured process for identifying, logging, escalating, resolving, and preventing future occurrences of system failures or cyber incidents.

---

## **Scope**

Applies to all IT systems, cloud infrastructure, servers, applications, and networks managed by APPNEURAL Pvt. Ltd. It covers all employees, IT administrators, and third-party service providers involved in system maintenance or support.

---

### **Objective**

* Minimize the duration and impact of unplanned system downtime.
* Ensure business continuity through a clear incident-handling framework.
* Strengthen preventive and recovery measures through post-incident learning.

---

### **Key Definitions**

* **Incident:** Any event that disrupts normal IT operations or system availability.
* **Downtime:** A period when a system, network, or service is unavailable or non-functional.
* **Emergency:** A high-severity event (e.g., data breach, ransomware, power outage) requiring immediate response and management escalation.
* **Incident Manager:** The designated person responsible for coordinating the incident response.

---

### **Roles & Responsibilities**

| Role                           | Responsibility                                                          |
| ------------------------------ | ----------------------------------------------------------------------- |
| **IT Support Team**            | Detect, log, and attempt to resolve incidents within defined SLAs.      |
| **Incident Manager**           | Classify severity, coordinate escalation, and oversee communication.    |
| **System Administrator**       | Perform diagnostics, restore services, and verify integrity.            |
| **Management/Leadership Team** | Approve emergency decisions and communicate to clients or stakeholders. |
| **All Employees**              | Promptly report observed IT issues or abnormalities to IT support.      |

---

### **Workflow Steps**

#### **1. Incident Identification & Logging**

* Any team member noticing abnormal behavior (e.g., system crash, slow performance, login issues) must **report immediately** to IT Support via email or ticketing system.
* IT Support logs the incident with:

  * **Time of detection**
  * **Description of issue**
  * **Affected systems/users**
  * **Severity level (Low/Medium/High/Critical)**

#### **2. Incident Classification**

| Severity     | Description                         | Response Time                | Example                     |
| ------------ | ----------------------------------- | ---------------------------- | --------------------------- |
| **Low**      | Minor issue, no major impact        | Within 8 hrs                 | Slow performance            |
| **Medium**   | Partial service disruption          | Within 4 hrs                 | One module down             |
| **High**     | Major service outage                | Immediate                    | Server crash                |
| **Critical** | Business-wide outage or data breach | Immediate + Management alert | Network failure, ransomware |

#### **3. Incident Escalation Procedure**

* If not resolved within defined timelines:

  * Escalate to **Incident Manager**.
  * Notify **Project Head or CTO** (for client-impacting issues).
  * Critical incidents trigger a **Crisis Response Meeting** within 30 minutes.

#### **4. System Restoration & Verification**

* Diagnose the **root cause** using system logs and monitoring tools.
* Execute **recovery procedures** (e.g., restoring from backup, restarting services, applying patches).
* Verify:

  * System functionality restored.
  * No data corruption or loss.
  * Dependent services are operational.
* Communicate restoration status to all affected stakeholders.

#### **5. Post-Incident Review & Documentation**

* Within **48 hours** after resolution, conduct a **Post-Incident Review Meeting**.
* Document:

  * Cause of incident
  * Steps taken to resolve
  * Preventive actions
  * Lessons learned
* Update the **Incident Log Register** and share learnings with relevant teams.

#### **6. Preventive & Continuous Improvement Actions**

* Analyze incident trends every quarter to identify recurring issues.
* Implement:

  * **System monitoring improvements**
  * **Patch updates**
  * **Hardware or network upgrades**
  * **Policy enhancements**

---

### **Incident Communication Protocol**

| Stage      | Communication Type                | Responsible      |
| ---------- | --------------------------------- | ---------------- |
| Detection  | Internal email/slack alert        | IT Support       |
| Escalation | Incident summary report           | Incident Manager |
| Resolution | Status update + root cause report | System Admin     |
| Closure    | Post-incident review report       | IT Head          |

**Client Notification (if applicable):**
If downtime impacts clients or live projects, an official notification (email/SMS) should be sent within 1 hour, including expected resolution time.

---

### **Emergency Handling Procedure**

For emergencies such as **cyberattacks, data breaches, or hardware failures**:

1. **Isolate affected systems** immediately (disconnect network access).
2. **Notify the Cybersecurity Team and Management.**
3. **Activate Disaster Recovery Plan (DRP)** if data is compromised.
4. **Engage third-party experts** if internal expertise is insufficient.
5. **Perform forensics** to identify the cause and restore from clean backups.
6. **Document full event report** and submit to IT Compliance Officer.

---

### **Best Practices**

✅ Maintain **real-time system monitoring dashboards** using tools like Grafana, Zabbix, or Datadog.

✅ Define **clear SLAs** for different severity levels.

✅ Conduct **quarterly disaster recovery drills.**

✅ Keep **redundant power, internet, and storage systems**.

✅ Perform **regular patch updates** to prevent system failures.

✅ Ensure **off-site and cloud backups** for critical systems.

✅ Maintain a **24/7 incident response contact list.**

✅ Review and test **Incident Response Plans (IRP)** biannually.

✅ Conduct **root cause analysis (RCA)** for all high-severity incidents.

---

### **Templates**

#### **1. Incident Log Template**

| Incident ID | Date/Time           | Reported By    | Affected System | Severity | Description              | Resolution Steps               | Downtime (hrs) | Root Cause     | Status |
| ----------- | ------------------- | -------------- | --------------- | -------- | ------------------------ | ------------------------------ | -------------- | -------------- | ------ |
| IT-INC-001  | 17/10/2025 11:15 AM | Rahul (DevOps) | Server 02       | High     | Application server crash | Restarted service & patched OS | 2              | Outdated patch | Closed |

#### **2. Post-Incident Review Report**

**Date:**
**Incident ID:**
**Summary:**
**Root Cause:**
**Resolution Summary:**
**Downtime Duration:**
**Business Impact:**
**Preventive Measures:**
**Prepared By:**
**Approved By:**

---

### **Compliance Reference**

* ISO/IEC 27001: Information Security Management
* NIST SP 800-61: Computer Security Incident Handling Guide
* Indian IT Act 2000 (Cyber Incident Response Requirements)

---

Would you like me to create the **next SOP (IT–08: Preventive Maintenance & System Health Monitoring)** in the same in-depth format with templates and best practices?
