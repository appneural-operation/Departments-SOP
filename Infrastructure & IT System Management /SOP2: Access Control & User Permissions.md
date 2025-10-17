# SOP: Access Control & User Permissions

### **Purpose:**

To define a standardized process for **creating, managing, reviewing, and revoking user access** to company systems, tools, and data.
The goal is to protect sensitive information, prevent unauthorized access, and ensure that every employee only has the access necessary to perform their job responsibilities.

---

### **Scope:**

This SOP applies to all employees, interns, contractors, and third-party service providers at **APPNEURAL Pvt. Ltd.** who are granted access to company systems, servers, networks, software tools, or confidential databases.

---

### **Definitions:**

* **Access Control:** The process of granting, monitoring, and restricting access to systems and data based on user roles.
* **RBAC (Role-Based Access Control):** A model where access permissions are assigned based on the user’s job role or function.
* **MFA (Multi-Factor Authentication):** A security mechanism that requires users to verify their identity using multiple authentication methods (e.g., password + OTP).
* **Access Matrix:** A master document listing who has access to what systems and at what level (view, edit, admin).
* **De-provisioning:** Revoking system access after an employee exits or changes roles.

---

## **Step-by-Step Workflow**

### **1. Access Request & Authorization**

* The employee or department head submits an **Access Request Form** to IT.
* The request includes:

  * Employee details (name, department, role)
  * System(s) or tool(s) to be accessed
  * Level of access required (read/write/admin)
  * Justification for access
* The **Manager or HR** verifies the need and approves the request.
* IT logs the approved request in the **Access Control Register.**

---

### **2. User Account Creation**

* IT creates user accounts as per the approved request.
* Assign permissions according to **Role-Based Access Control (RBAC)** — e.g.:

  * Developer → access to GitHub, Jira
  * HR → access to HRMS, Payroll system
  * Finance → access to Accounting software
* Default password is generated and shared via secure channel (e.g., company password manager).
* User is required to **reset password upon first login** and enable **MFA.**

---

### **3. Access Modification**

* Any access changes (promotion, department transfer, role switch) must be requested formally through the **Access Modification Form.**
* Manager approves modification; IT implements it within 24 hours.
* IT updates the **Access Control Register** with the new permissions.

---

### **4. Access Review (Quarterly)**

* IT conducts a **quarterly access review** with department heads.
* Validate that access is still relevant for each employee.
* Remove inactive users or redundant privileges.
* Generate a **Quarterly Access Audit Report** and share it with Operations & HR.

---

### **5. Access Revocation (Exit or Role Change)**

* HR notifies IT immediately upon resignation, termination, or role change.
* IT revokes system and tool access **within 24 hours** of exit.
* Retrieve all company credentials from the employee (passwords, tokens).
* Disable accounts from email, project tools, repositories, and cloud services.
* Record revocation in **Access Control Register** and mark as “Closed.”

---

### **6. Multi-Factor Authentication (MFA) Enforcement**

* All administrative or confidential systems (e.g., email, GitHub, financial tools) **must have MFA enabled.**
* IT periodically audits MFA compliance.
* Employees found not enabling MFA will be restricted from accessing critical systems until compliance.

---

### **7. Access Audit & Reporting**

* Conduct **bi-annual internal access audits.**
* Verify that:

  * Access levels match the employee’s current role.
  * Former employees’ accounts are deactivated.
  * MFA and password policies are enforced.
* Generate a report with audit findings, non-compliance areas, and corrective actions.

---

## **Roles & Responsibilities**

| Role                     | Responsibilities                                                         |
| ------------------------ | ------------------------------------------------------------------------ |
| **IT Manager**           | Approves access policies, oversees audits, and ensures compliance.       |
| **System Administrator** | Creates/modifies/deactivates accounts, maintains logs, and enforces MFA. |
| **Department Head**      | Approves access requests and validates relevance during audits.          |
| **HR Department**        | Notifies IT on new hires, exits, or role changes.                        |
| **Employee**             | Uses credentials responsibly and does not share login information.       |

---

## **Templates & Forms**

### **Template 1 – Access Request Form**

| Field                 | Details               |
| --------------------- | --------------------- |
| Employee Name         |                       |
| Department            |                       |
| Designation           |                       |
| System/Tool Requested |                       |
| Access Type           | (View / Edit / Admin) |
| Justification         |                       |
| Manager Approval      |                       |
| IT Action Taken       |                       |
| Date of Creation      |                       |

---

### **Template 2 – Access Modification Form**

| Field              | Details |
| ------------------ | ------- |
| Employee Name      |         |
| Department         |         |
| Current Access     |         |
| Requested Change   |         |
| Reason for Change  |         |
| Manager Approval   |         |
| IT Completion Date |         |

---

### **Template 3 – Access Revocation Checklist**

| Checklist Item              | Status |
| --------------------------- | ------ |
| Email Account Deactivated   | ✅ / ❌  |
| Project Tool Access Removed | ✅ / ❌  |
| Cloud Access Revoked        | ✅ / ❌  |
| Passwords Reset             | ✅ / ❌  |
| MFA Disabled                | ✅ / ❌  |
| Final Verification Logged   | ✅ / ❌  |

---

## **Tools Used**

* Google Workspace Admin Console
* GitHub / GitLab User Management
* Jira / ClickUp / Slack Admin Panels
* Password Manager (Bitwarden / 1Password)
* Access Control Register (Google Sheet or Notion Database)

---

## **Best Practices**

* Follow **Least Privilege Principle (LPP):** Only grant necessary permissions.
* Enforce **MFA on all critical systems.**
* Review and clean inactive accounts quarterly.
* Use **role-based groups** instead of individual permissions where possible.
* Do not share credentials via email, chat, or unsecured files.
* Maintain **access logs** for at least 1 year for audit trail.
* Immediately revoke access upon employee termination.

---

## **Key Performance Indicators (KPIs)**

* % of employees with MFA enabled
* % of users reviewed during quarterly audit
* Time taken to revoke access after exit (Target: < 24 hours)
* Number of unauthorized access attempts per quarter
* Number of overdue access reviews

---

## **Audit & Compliance**

* Adhere to:

  * **Information Technology Act, 2000 (India)**
  * **ISO 27001 – Information Security Management System (ISMS)**
  * **GDPR (if handling client data from EU)**
* Conduct **internal access review audits** twice a year.


