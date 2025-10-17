#  SOP: Software Installation & Patch Management

### **Purpose:**

To establish a standardized procedure for **installing, maintaining, updating, and removing software** on company systems.
This SOP ensures that only **approved, licensed, and secure software** is used within APPNEURAL Pvt. Ltd. and that all systems are **regularly patched** to prevent vulnerabilities and maintain performance.

---

### **Scope:**

This SOP applies to:

* All company-owned laptops, desktops, and servers.
* All departments (Development, HR, Finance, Operations, etc.) using company systems.
* IT personnel responsible for software management and system maintenance.

---

### **Definitions:**

* **Patch:** A software update designed to fix security vulnerabilities, bugs, or performance issues.
* **Approved Software List (ASL):** The list of company-approved applications authorized for use.
* **Version Control:** Tracking and managing changes or updates to software versions.
* **Obsolete Software:** Applications no longer supported or required by the company.
* **Unauthorized Software:** Any software installed without IT department approval.

---

## **Step-by-Step Workflow**

### **1. Software Request & Approval**

* The employee submits a **Software Installation Request Form** to the IT department.
* The form includes:

  * Software name, version, and purpose.
  * Justification for use.
  * Department and requester details.
* The **Department Head and IT Manager** review the request.
* IT verifies:

  * Software licensing and security risks.
  * Compatibility with existing systems.
* If approved, software is added to the **Approved Software List (ASL)** and installed.

---

### **2. Installation Process**

* IT installs the software using official vendor sources or licensed installers.
* Installation steps are documented in the **Software Installation Log**.
* Assign appropriate permissions (admin/user level) based on employee role.
* Perform a post-installation verification test to ensure functionality.
* Update the **Asset Inventory Register** with the installed software details.

---

### **3. Software Version Control**

* Maintain a **Software Version Tracker** (Excel/Notion/ITSM tool).
* Record:

  * Software name and version
  * Installation date
  * License expiry date
  * Latest patch/update applied
* The tracker helps identify outdated or vulnerable versions for timely updates.

---

### **4. Patch Management**

* IT monitors vendors’ websites or automated patch management tools weekly for updates.
* Patches are classified as:

  * **Critical Security Patches** – apply within 48 hours
  * **Regular Updates** – apply monthly
  * **Feature Enhancements** – apply as per business need
* IT tests major patches in a sandbox environment before deploying company-wide.
* Maintain a **Patch Deployment Log** with details of applied updates.

---

### **5. Software Audit & Compliance**

* Conduct a **bi-annual software audit** to verify:

  * Only approved software is installed.
  * All licenses are valid and renewed.
  * No unauthorized or pirated software is in use.
* Generate a **Software Audit Report** and share it with management.
* Any unapproved software must be removed immediately.

---

### **6. Removal of Obsolete or Unauthorized Software**

* Identify outdated, unsupported, or unauthorized software during audits or patch reviews.
* IT notifies the department head and uninstalls the software.
* Record the removal in the **Software Decommission Log.**
* Update the **Asset Inventory Register** and remove license entries.

---

### **7. Documentation & Reporting**

All actions related to software management must be recorded in:

* **Software Installation Log**
* **Patch Deployment Log**
* **Software Decommission Log**
* **Software Audit Report**

Reports are submitted to the IT Manager and reviewed quarterly.

---

## **Roles & Responsibilities**

| Role                     | Responsibilities                                                    |
| ------------------------ | ------------------------------------------------------------------- |
| **IT Manager**           | Approves software, oversees patch management and audits.            |
| **System Administrator** | Installs software, applies patches, maintains version control logs. |
| **Department Head**      | Approves software requests from team members.                       |
| **Employee**             | Requests only approved software, reports issues promptly.           |
| **Finance/Procurement**  | Manages software licensing and renewals.                            |

---

## **Templates & Forms**

### **Template 1 – Software Installation Request Form**

| Field                | Details     |
| -------------------- | ----------- |
| Requester Name       |             |
| Department           |             |
| Software Name        |             |
| Version              |             |
| Purpose of Use       |             |
| License Type         | Free / Paid |
| Manager Approval     |             |
| IT Review & Approval |             |
| Installation Date    |             |
| Installed By         |             |

---

### **Template 2 – Patch Deployment Log**

| Field         | Details                        |
| ------------- | ------------------------------ |
| Software Name |                                |
| Version       |                                |
| Patch Type    | (Security / Regular / Feature) |
| Date Applied  |                                |
| Applied By    |                                |
| Verified By   |                                |
| Notes         |                                |

---

### **Template 3 – Software Decommission Log**

| Field              | Details                            |
| ------------------ | ---------------------------------- |
| Software Name      |                                    |
| Version            |                                    |
| Reason for Removal | Obsolete / Unauthorized / Replaced |
| Date of Removal    |                                    |
| Removed By         |                                    |
| Approved By        |                                    |

---

## **Tools Used**

* **Patch Management Tools:** Microsoft Intune, ManageEngine Patch Manager, or WSUS
* **License Tracking:** Excel, Zoho Creator, or Asset Tiger
* **Version Control Tracker:** Google Sheets or Notion database
* **Security Scanner:** Windows Defender / Avast Business / CrowdStrike

---

## **Best Practices**

* Always use **licensed and vendor-approved installers.**
* Test patches in a non-production environment before deployment.
* Maintain **automated reminders** for software license renewals.
* Enforce **least privilege installation policy** (only IT can install software).
* Regularly backup configurations before major updates.
* Schedule **monthly patch reviews** and track compliance.

---

## **Key Performance Indicators (KPIs)**

* % of systems with latest patches applied
* Number of unauthorized software incidents
* Average time to deploy critical patches (Target: < 48 hrs)
* Number of expired software licenses per quarter
* Compliance rate with Approved Software List

---

## **Audit & Compliance**

* Follow security standards under:

  * **Information Technology Act, 2000 (India)**
  * **ISO/IEC 27001 – Information Security Management**
  * **CMMI / NIST Patch Management Frameworks**
* Maintain audit records for **minimum 3 years**.

---

## **Example Report Summary (Quarterly IT Report)**

| Category              | Total | Compliant | Non-Compliant | Action Taken              |
| --------------------- | ----- | --------- | ------------- | ------------------------- |
| Software Updates      | 42    | 40        | 2             | Pending patches scheduled |
| Unauthorized Software | 3     | -         | 3             | Removed                   |
| License Renewals      | 5     | 5         | -             | All renewed               |
| Critical Patches      | 15    | 15        | -             | Completed                 |

---

