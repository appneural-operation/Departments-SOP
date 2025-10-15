# SOP: Code Review, Testing & Deployment

## 1. Purpose
This SOP defines a **comprehensive and standardized workflow** for code review, testing, and deployment to ensure:  
- **High-quality, secure, and maintainable code**  
- Compliance with **DevSecOps principles, ISTQB QA standards, and security frameworks (OWASP, GDPR, ISO 27001)**  
- Efficient **CI/CD deployment** with rollback capabilities  
- Clear **accountability, traceability, and documentation**  

It serves as a **single source of truth** for developers, QA, DevOps, and project management.

---

## 2. Scope
Applicable to:  
- All **software development projects** at APPNEURAL Pvt. Ltd.  
- All team members involved in **coding, reviewing, testing, and deploying software**  
- **Environments:** Development (Dev), Staging, and Production  
- Includes **peer code reviews, automated/manual testing, CI/CD deployment, and post-deployment monitoring**

---

## 3. Roles & Responsibilities

| Role | Responsibilities |
|------|-----------------|
| Developer | Write code following standards, add unit tests, submit Pull Requests (PRs) |
| Peer Reviewer / Senior Developer | Review code for correctness, security, maintainability; approve PRs |
| QA / Tester | Execute unit, integration, regression, and UAT tests; log defects |
| DevOps Engineer | Deploy code using CI/CD pipelines, validate environment, manage rollback |
| Product Owner / PM | Approve UAT, confirm feature readiness for production |
| Security Officer / Compliance | Conduct security scans, ensure compliance (OWASP/GDPR/ISO 27001) |

---

## 4. Tools Used
- **Version Control:** GitHub, GitLab, Bitbucket  
- **CI/CD:** Jenkins, GitHub Actions, GitLab CI, Azure DevOps  
- **Testing:** Unit testing frameworks (JUnit, PyTest, Jest), integration and regression suites  
- **Security:** SonarQube, Snyk, OWASP ZAP, Fortify  
- **Collaboration & Documentation:** Microsoft Teams, SharePoint, Jira, Confluence  
- **Time & Progress Tracking:** Toggl, Clockify  

---

## 5. Code Review Process (Step-by-Step)

**Objective:** Ensure all code is **functional, secure, readable, and maintainable** before merging.

**Step 1: Code Submission**
- Developer completes feature/fix and pushes code to a **feature branch**  
- Add **meaningful commit messages** describing changes

**Step 2: Pull Request (PR) Creation**
- Create PR targeting **development/main branch**  
- Include **description, linked task ID, screenshots, and testing notes**

**Step 3: Peer Review**
- **1–2 peers** review the code  
- Check for:  
  - Correctness and functionality  
  - Code style, naming conventions, readability  
  - Performance and optimization  
  - Security vulnerabilities (OWASP checklist)  
  - Unit tests coverage  

**Step 4: Approval & Merge**
- PR approved if **all criteria pass**  
- Merge using **squash/rebase** as per standard  
- **Failed PR:** Developer addresses review comments and resubmits  

**Step 5: Documentation**
- All PR comments and approvals logged in **GitHub/GitLab**  
- Link PR to Jira/SharePoint for **traceability**

**Checklist: Code Review**
```

## Code Review Checklist

Feature/Task: [ID & Description]
Developer: [Name]
Reviewer: [Name]

1. Functionality: [✔/✖] – Comments:
2. Code Style & Standards: [✔/✖] – Comments:
3. Security Compliance (OWASP/GDPR/ISO): [✔/✖] – Comments:
4. Unit Tests Coverage: [✔/✖] – Comments:
5. Documentation / Comments: [✔/✖] – Comments:
6. Approval Status: [Approved / Changes Required]

```

---

## 6. Testing Process (Step-by-Step)

**Objective:** Verify the code is **correct, reliable, secure, and meets requirements**

**Step 1: Unit Testing**
- Developer writes and executes **unit tests** locally  
- Test individual functions/modules for correctness

**Step 2: Integration Testing**
- QA executes tests to validate **interaction between modules**  
- Check data flow, API integration, and system behavior

**Step 3: Regression Testing**
- QA ensures **existing features are unaffected**  
- Automated or manual regression suites run on staging environment

**Step 4: User Acceptance Testing (UAT)**
- PO or stakeholders validate features in **staging environment**  
- Approve only after **all acceptance criteria are met**

**Step 5: Logging Results**
- Use Jira, TestRail, or SharePoint for **test results and defect tracking**  
- Assign defects to developers for resolution

**Checklist: Testing**
```

## Testing Checklist

Feature/Task: [ID & Description]
Environment: [Dev / Staging / Production]
Tester: [Name]

Unit Test: [✔/✖] – Comments:
Integration Test: [✔/✖] – Comments:
Regression Test: [✔/✖] – Comments:
UAT Approval: [✔/✖] – Comments:
Security Checks: [✔/✖] – Comments:

```

---

## 7. Deployment Process (Step-by-Step)

**Objective:** Deploy code **safely and efficiently** with rollback capability.

**Step 1: Pre-Deployment Checks**
- PR approved and all tests passed  
- Security scans cleared  
- Environment variables and configuration verified  

**Step 2: CI/CD Deployment**
- Execute deployment using **Jenkins / GitHub Actions / GitLab CI**  
- Deploy first to **staging** for final verification  
- Deploy to **production** only after QA & PO approval  

**Step 3: Post-Deployment Monitoring**
- Monitor logs, errors, performance metrics  
- Communicate success or issues via **Microsoft Teams / Email**

**Step 4: Rollback Procedure**
- If production issue occurs, rollback to **previous stable build**  
- Document incident, root cause, and resolution  

**Checklist: Deployment**
```

## Deployment Checklist

Feature/Task: [ID & Description]
Environment: [Dev / Staging / Production]
Deployer: [Name]

Pre-Deployment Checks:

* PR Approved: [✔/✖]
* Tests Passed: [✔/✖]
* Security Scan: [✔/✖]

Deployment Steps:

* CI/CD Pipeline Executed: [✔/✖]
* Staging Validation: [✔/✖]
* Production Deployment: [✔/✖]

Post-Deployment Monitoring:

* Logs Checked: [✔/✖]
* Metrics OK: [✔/✖]

Rollback Needed: [Yes/No] – Action Taken: [Details]

```

---

## 8. Security & Compliance
- **OWASP Top 10:** Validate all PRs for vulnerabilities  
- **GDPR / ISO 27001:** Ensure sensitive data is handled securely  
- Conduct automated security scans via **SonarQube, Snyk, or Fortify**  
- Log all findings in **SharePoint / Jira**  

---

## 9. Reporting & Documentation
- **Code Review Logs:** PR approvals and comments  
- **Testing Reports:** Unit, integration, regression, and UAT results  
- **Deployment Logs:** CI/CD execution and post-deployment monitoring  
- All documents stored in **SharePoint / Teams** for audit and traceability  

---

## 10. Continuous Improvement
- SOP reviewed every **6 months** or after critical issues  
- Collect feedback from **developers, QA, DevOps, and PO**  
- Update process for **higher efficiency, faster deployment, and better quality**

---

## 11. References
- DevSecOps Principles: https://www.devsecops.org  
- ISTQB Testing Standards: https://www.istqb.org  
- OWASP Top 10: https://owasp.org/Top10/  
- ISO 27001: https://www.iso.org/isoiec-27001-information-security.html  
- CI/CD Pipeline Guides: Jenkins, GitHub Actions, GitLab CI  


