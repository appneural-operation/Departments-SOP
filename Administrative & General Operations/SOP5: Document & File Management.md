# SOP 5: Document & File Management

### **Purpose:**  
To establish a standardized and secure structure for storing, naming, sharing, and managing all company documents and files across digital platforms like **Google Drive, GitHub, and internal systems**, ensuring easy accessibility, version control, and data security.

---

## **1. Scope**
This SOP applies to all departments and employees at **APPNEURAL Pvt. Ltd.** who create, access, or manage digital files and documents. It covers:  
- File creation and naming conventions  
- Folder structuring across Google Drive and GitHub  
- Access control and permissions  
- Version control and backup  
- Archiving and deletion policies  

---

## **2. Objectives**
- Maintain organized, clutter-free digital storage.  
- Ensure employees can easily locate required documents.  
- Protect confidential data from unauthorized access.  
- Maintain accurate and updated versions of all files.  
- Promote uniformity across all repositories.  

---

## **3. Roles & Responsibilities**

| Role | Responsibility |
|------|----------------|
| **Admin Department** | Create and maintain master folder structure, monitor access permissions, and conduct audits. |
| **Department Heads** | Ensure departmental folders are updated and properly structured. |
| **Employees/Interns** | Follow naming conventions, store files in correct folders, and maintain version discipline. |
| **IT Department** | Manage backups, storage capacity, and security permissions. |
| **Operations Manager** | Review and approve folder restructuring or access changes. |

---

## **4. Folder Structure Guidelines**

### **A. Google Drive Folder Structure**
All company documents must be organized under a shared drive named:  
📂 **APPNEURAL Pvt. Ltd. – Central Repository**

**Example Folder Structure:**
```

APPNEURAL Pvt. Ltd. – Central Repository
│
├── 01_HR & Administration
│   ├── Employee Records
│   ├── Policies & Handbooks
│   ├── Recruitment & Onboarding
│   ├── Attendance & Leave Data
│
├── 02_Product Development
│   ├── Frontend
│   ├── Backend
│   ├── Testing
│   ├── Deployment
│
├── 03_Operations
│   ├── SOPs
│   ├── Audits
│   ├── Vendor Management
│
├── 04_Finance
│   ├── Invoices
│   ├── Payroll
│   ├── Budgeting
│
├── 05_Marketing
│   ├── Campaigns
│   ├── Social Media Assets
│   ├── Reports
│
└── 06_Projects
├── Client A
├── Client B
└── Client C

```

📌 **Rule:** No personal folders or unapproved files should be stored in the shared drive.

---

### **B. GitHub Folder Structure**
All company project files hosted on GitHub must follow a clear hierarchy to ensure collaboration efficiency and data security.

**Example:**
```

APPNEURAL-Projects/
│
├── CoreHRAdministrationSOPs/
│   ├── SOP1-SOPManagement.md
│   ├── SOP2-EmployeeRecordKeeping.md
│
├── AdministrativeOperationsSOPs/
│   ├── SOP1-AssetManagement.md
│   ├── SOP2-OfficeMaintenance.md
│
├── ProductDevelopment/
│   ├── Frontend/
│   ├── Backend/
│   ├── Documentation/
│
└── ReadMe.md

```

📌 **Rules:**
- Use proper folder naming (no spaces, use underscores).  
- Maintain `.md` files for documentation.  
- Upload only reviewed and approved files.  
- Store draft files locally or on temporary branches.

---

## **5. File Naming Conventions**

### **Format:**
`Department_ProjectName_DocumentType_Version_Date`

**Examples:**
- `HR_InternPolicy_V1_2025-10-20`  
- `Dev_FrontendDesignDoc_V2_2025-09-15`  
- `Ops_AssetRegister_V3_2025-08-30`

📌 **Guidelines:**
- Use **underscores (_) or camel case** instead of spaces.  
- Include **version number** (V1, V2, etc.) and **date** (YYYY-MM-DD).  
- Avoid abbreviations unless department-approved.

---

## **6. Version Control & Updates**

| Activity | Responsibility | Frequency |
|-----------|----------------|------------|
| Create new version after major update | File Owner | As needed |
| Maintain “Version History” sheet in Drive | Admin | Continuous |
| Archive old versions (if outdated) | Admin | Monthly |
| Review for obsolete files | Department Head | Quarterly |

📌 **Rule:**  
Do not overwrite existing files — always create a new version and archive the old one in a folder named **“Old Versions”**.

---

## **7. Access Control & Permissions**

| Type of Access | Who Gets It | Notes |
|----------------|-------------|-------|
| **View Only** | Interns, external stakeholders | No download/edit rights |
| **Edit Access** | Core team members, department heads | Restricted to active users only |
| **Admin Access** | Operations Manager, Admin, IT | Full control and permission management |

📌 **Best Practice:** Use Google Shared Drives instead of individual folders to ensure continuity even if employees leave.

---

## **8. Data Backup & Security**
- Weekly automatic backups for Google Drive and GitHub repositories.  
- IT/Admin must maintain a **secondary encrypted backup**.  
- Backup credentials to be held by **Operations Manager and IT Head only**.  
- Sensitive HR or financial files must have restricted access.  
- Never share confidential documents via personal email or WhatsApp.

---

## **9. Archiving & Deletion Policy**
- **Inactive projects** archived in “Archived – YYYY” folders.  
- **Old files (1+ year)** reviewed and deleted after management approval.  
- **Confidential data** deleted securely through IT-managed processes.  
- Maintain an **Archive Log Sheet** for all deletions and archives.

---

## **10. Review & Monitoring**
- **Quarterly audits** by Admin on folder structures and access permissions.  
- Department Heads ensure all documents are updated and properly stored.  
- Non-compliance reports submitted to Operations Manager for correction.

---

## **11. Templates & Tools**

| Purpose | Tool/Template |
|----------|---------------|
| File Naming Reference | File Naming Sheet (Google Sheet) |
| Folder Structure Reference | Company Folder Hierarchy Document |
| Access Control Tracker | Permission Sheet |
| Archive & Version Tracker | Document Archive Sheet |
| Backup Verification | Weekly Backup Log |

---

## **12. Best Practices**

### **General Practices**
- Always store files in designated department folders.  
- Avoid duplicate or redundant copies.  
- Delete drafts and temporary files monthly.  

### **Naming & Version Control**
- Maintain a “Change Log” inside important files.  
- Add file owner initials for traceability (e.g., `HR_LeavePolicy_PR_V2_2025-10-21`).  

### **Access & Security**
- Use company emails for sharing and collaboration.  
- Never grant personal Gmail or external access without approval.  
- Use “Viewer” access for clients or external vendors.  

### **Backup & Recovery**
- Conduct bi-weekly verification of backups.  
- Store sensitive ZIP files in encrypted form if necessary.  

### **Review Discipline**
- Departments review folder organization every 30 days.  
- HR/Admin send monthly “Document Clean-up Reminder” emails.  

### **GitHub Maintenance**
- Only merge reviewed pull requests.  
- Protect main branches from direct commits.  
- Include a `README.md` in every major folder describing its contents.  

---
