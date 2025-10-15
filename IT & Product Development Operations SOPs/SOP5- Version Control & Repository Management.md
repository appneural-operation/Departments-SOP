# SOP: Version Control & Repository Management (GitHub/GitLab)

## 1. Purpose
This SOP establishes a **standardized approach to manage code repositories** to ensure:  
- **Code integrity, traceability, and security**  
- Efficient collaboration among development teams  
- Compliance with **company confidentiality, NDA, and IT Act 2000**  
- Consistency in **branching, versioning, and release management**  
- Reliable **backup and archival** of code  

---

## 2. Scope
Applies to:  
- All **software projects** hosted on GitHub/GitLab repositories  
- All developers, QA, DevOps, and project managers with repository access  
- All types of branches: **Main, Development, Feature, Hotfix, Release**  

---

## 3. Reference Frameworks
- **Gitflow Workflow Model** (Vincent Driessen)  
- **Semantic Versioning (SemVer) Standards**  
- **Company Confidentiality Policy, NDA, and IT Act 2000 compliance**  
- **Internal QA, DevOps, and code security standards**  

---

## 4. Roles & Responsibilities

| Role | Responsibilities |
|------|-----------------|
| Repository Owner | Create repositories, define access permissions, manage backups |
| Developer | Work on assigned branches, follow commit conventions, create PR/MR |
| Reviewer / Team Lead | Approve pull/merge requests, ensure code quality and standards |
| DevOps Engineer | Merge approved PRs, manage CI/CD integration, implement rollback |
| Security Officer / Compliance | Ensure repository access, enforce NDA and IT security compliance |

---

## 5. Repository Structure & Branching Strategy

**Standard Branch Types (Gitflow-based):**  
1. **Main / Master:** Stable production-ready code only  
2. **Development (Dev):** Integration branch for completed features and fixes  
3. **Feature Branches:** Created from Dev for new features (`feature/<feature-name>`)  
4. **Hotfix Branches:** Created from Main for urgent fixes (`hotfix/<issue>`)  
5. **Release Branches (Optional):** For staging/production release prep (`release/<version>`)

**Workflow Guidelines:**  
- Feature branches **merge only into Dev**  
- Hotfix branches **merge into Main and Dev**  
- Release branches **merge into Main and Dev** after QA approval  
- Avoid direct commits to Main (except emergency hotfixes)

---

## 6. Branch Naming Conventions

| Branch Type | Naming Convention |
|-------------|------------------|
| Feature | `feature/<short-description>` (e.g., `feature/user-login`) |
| Hotfix | `hotfix/<issue-id>` (e.g., `hotfix/1234-crash-fix`) |
| Release | `release/<version>` (e.g., `release/1.2.0`) |
| Development | `dev` |
| Main | `main` |

> Branch names should be **lowercase, hyphen-separated, and descriptive**.

---

## 7. Commit Message Conventions

**Structure:**  
```

<type>(<scope>): <short description>

<body> (optional)
- Details of changes
- Issue ID reference
```

**Type Examples:**

* `feat` → New feature
* `fix` → Bug fix
* `docs` → Documentation changes
* `chore` → Maintenance tasks
* `refactor` → Code restructuring

**Example:**

```
feat(auth): add JWT token validation
- Implemented middleware for token verification
- Linked to Jira ticket #123
```

**Commit Guidelines:**

* Write **clear, descriptive messages**
* Reference **task or bug ID**
* **Atomic commits:** one logical change per commit

---

## 8. Pull/Merge Request Policy

**Process:**

1. Developer submits PR/MR from Feature/Hotfix branch to Dev/Main
2. **Peer review** required by at least one senior developer or team lead
3. Check for:

   * Code quality and standards
   * Unit and integration test coverage
   * Security compliance (NDA, IT Act, OWASP)
4. PR approved → Merged using **Squash/Merge/Rebase strategy**
5. Merge must include **linked issue/task ID** for traceability

**Template for PR Description:**

```
Title: <Feature/Hotfix short description>

Description:
- What is implemented or fixed
- Issue/Ticket ID: #1234
- Steps to test

Checklist:
- [ ] Code follows standards
- [ ] Unit tests added
- [ ] Security check passed
- [ ] Documentation updated
```

---

## 9. Access Control & Permissions

**Permission Matrix:**

| Role                          | Push                | Merge PR/MR                     | Delete Branch             |
| ----------------------------- | ------------------- | ------------------------------- | ------------------------- |
| Developer                     | Feature/Hotfix only | Cannot merge to Dev/Main        | Cannot delete branches    |
| Team Lead / Reviewer          | Feature/Hotfix      | Can approve & merge to Dev/Main | Cannot delete Main        |
| DevOps / Repo Admin           | All                 | All                             | Can delete stale branches |
| Security Officer / Compliance | Read                | Review for compliance           | No delete rights          |
| PM / Product Owner            | Read                | Review for functionality        | No delete rights          |

> Access is granted through **GitHub/GitLab Teams** and **2FA authentication enforced**.

---

## 10. Backup & Archival Policy

**Frequency & Retention:**

* Automatic **daily backups** of all repositories via GitLab/GitHub backup tools or scripts
* **Monthly snapshot** archived in SharePoint or company cloud storage
* Retain **backups for at least 2 years**
* **Branch archival:** Delete feature/release branches post-merge, tag release before deletion

**Disaster Recovery:**

* Restore repository from backup in case of accidental deletion or corruption
* Validate integrity of restored code before redeployment

---

## 11. Version Tagging Standards (Semantic Versioning)

**Format:** `MAJOR.MINOR.PATCH`

* **MAJOR:** Breaking changes
* **MINOR:** New features (backward compatible)
* **PATCH:** Bug fixes / minor changes

**Tag Guidelines:**

* Tag release branch or commit merged into Main
* Example: `v1.2.0`, `v2.0.1-hotfix`
* Include **release notes and Jira/Bug IDs in tag description**

---

## 12. Security & Confidentiality Compliance

* All repositories are **private** by default
* Developers must sign **NDA** before access
* Sensitive data (API keys, passwords) must **never be committed**
* Enforce **branch protection rules**: require PR review, pass CI tests
* Comply with **IT Act 2000** and internal company data security policies
* Conduct **periodic audits** for access, code leaks, and vulnerabilities

---

## 13. CI/CD Integration & Repository Management

* **Development branches** linked to CI/CD pipeline for automated tests
* **Main branch** triggers deployment pipeline to Production (after QA approval)
* Automated notifications to **Teams / Email** on build status, PR approval, or merge
* Use **protected branches and review approvals** to prevent accidental merges

---

## 14. Documentation & Reporting

* Maintain **branch, commit, and PR logs** in GitHub/GitLab
* Archive **release notes, version tags, and deployment history** in SharePoint / Confluence
* Report **inactive/stale branches** monthly for cleanup
* Maintain **audit trail for security compliance and traceability**

---

## 15. Continuous Improvement

* Conduct **quarterly code repository audits**
* Update **branching strategy, commit conventions, and backup procedures** as needed
* Conduct team training on **Gitflow, versioning, and repository best practices**
* Review **release notes and tag management** for improved deployment efficiency

---

## 16. References

* Gitflow Workflow Model: [https://nvie.com/posts/a-successful-git-branching-model/](https://nvie.com/posts/a-successful-git-branching-model/)
* Semantic Versioning: [https://semver.org/](https://semver.org/)
* GitHub / GitLab Official Documentation
* ISO/IEC 27001 & IT Act 2000 (Data Security Guidelines)
* Internal NDA and Confidentiality Policies
