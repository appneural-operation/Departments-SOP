# 🛠️ SOP7: System Downtime, Incident & Emergency Handling 

**Purpose:**
Minimize downtime and ensure rapid, organized recovery from IT incidents by defining how incidents are identified, logged, escalated, remediated, and reviewed.

**Scope:**
Applies to all IT systems, applications, networks, cloud services, and endpoints at APPNEURAL Pvt. Ltd. Covers incidents (partial degradation) through emergencies (major outages, security breaches).

---

## 🔎 Definitions & Severity Levels

* **Incident:** Any event that disrupts normal operation (e.g., slow systems, failed backups, single-user outage).
* **Major Incident / Emergency:** Widespread outage, production system failure, data breach, or an incident impacting business-critical operations or clients.
* **SLA:** Target times for detection, response, and restoration.

**Severity matrix (example):**

* **P1 — Critical / Emergency:** Production down for all users, data loss, security breach.

  * Detection → Immediate, Response SLA = 15–30 minutes, Restore target = ≤4 hours (RTO goal depending on system).
* **P2 — High:** Major functionality degraded for many users.

  * Response SLA = 1 hour, Restore target = 8–24 hours.
* **P3 — Medium:** Limited user impact, workaround available.

  * Response SLA = 4 hours, Restore target = 48–72 hours.
* **P4 — Low:** Non-urgent issues, minor user inconvenience.

  * Response SLA = 2 business days, Restore target = next scheduled maintenance.

---

## 📞 Incident Communication & Escalation Overview

1. **Detect → Log → Triage → Contain → Restore → Communicate → Close → Review.**

2. **Escalation ladder (example):**

* **Level 0:** User / Helpdesk (first contact).
* **Level 1:** System Administrator / On-call Engineer.
* **Level 2:** Senior Engineer / IT Manager.
* **Level 3:** IT Head / CTO and Operations Head (for P1/P2).
* **External:** Vendor / Cloud provider / Security vendor (if required).

3. **Notification channels:** Pager/phone call → Teams/Slack incident channel → Email → Management call (for P1).

---

## ✅ Step-by-Step Procedures

### Step 1 — Incident Identification & Logging

**Who:** Any user / Helpdesk / Monitoring tool
**How:**

* Automated alert (monitoring, SIEM, backup failure) OR user report to helpdesk.
* Create an **Incident Ticket** immediately in your ITSM system (Jira Service Desk, Zoho Desk, ServiceNow) or Incident Log spreadsheet if ITSM unavailable.

**Incident Ticket minimum fields:**

```
- Incident ID
- Reporter & Contact
- Date/Time detected
- Affected system(s)/service(s)
- Brief description of issue
- Severity (initial)
- Number of users affected
- Attached logs/screenshots (if any)
```

**Template — Quick Incident Log (one-page):**

```
Incident ID: INC-2025-###
Reported By: [Name, Dept]
Date/Time: DD/MM/YYYY HH:MM
System Affected: [e.g., Prod-API]
Severity: P1 / P2 / P3 / P4
Summary: [2-line summary]
Immediate Action Taken: [Isolated server / Disabled account / Rebooted]
Assigned To: [Engineer Name]
Status: Open / In Progress / Resolved
```

---

### Step 2 — Triage & Classification

**Who:** On-call engineer / Level 1
**Actions:**

* Validate the incident (is it real or false positive?).
* Determine Severity using impact & business criticality.
* If P1/P2, **trigger Major Incident process** (paging, war-room).
* Assign owner and required parties (DBA, network, app owner, security).

**Checklist for triage:**

* Is core business affected? (Yes = escalate)
* Are backups intact? (Yes/No)
* Is data loss suspected? (Yes/No)
* Can users work around it? (Yes/No)

---

### Step 3 — Containment & Immediate Mitigation

**Who:** Assigned engineer(s), IT Manager if P1
**Actions:**

* Isolate affected systems or network segments to prevent spread.
* Apply temporary workarounds (redirect traffic, enable failover, use cached data).
* If security incident: preserve evidence (do not power off unless instructed), capture memory / logs, isolate compromised hosts.

**Containment principles:**

* Act fast; prioritize business continuity.
* Use documented runbooks for common outage types (DNS, database crash, application hang).
* Document every action taken in the incident ticket.

---

### Step 4 — Root Cause Diagnosis & Remediation

**Who:** Assigned technical team (Level 1/2/3)
**Actions:**

* Collect logs, error traces, monitoring graphs, recent deployments/changes.
* Execute diagnostic steps from runbook (e.g., check CPU/memory, disk I/O, DB locks, queue lengths).
* If patch/rollback required, follow change control for emergency changes (document and seek post-hoc approval if necessary).
* Apply fix and validate functionality with test cases or smoke tests.

**Emergency change controls:**

* Emergency change form completed in ticket (who, what, why).
* Dual authorization for critical changes (IT Manager + Ops Head).

---

### Step 5 — Restore & Validate

**Who:** Technical lead & QA support (if needed)
**Actions:**

* Restore services (restart, failover, restore from backup).
* Validate by running test transactions or having users confirm normal operation.
* Monitor systems closely for recurrence for a defined period (e.g., 4–24 hours).

**Restore checklist:**

* Service responding to health checks
* No data corruption detected
* Performance metrics back to baseline
* User signoff (for client-facing services)

---

### Step 6 — Communication (internal & external)

**Who:** Incident Owner / IT Manager / Communications Lead
**Actions & cadence:**

* **Initial acknowledgement** to stakeholders within Response SLA (e.g., 15 min for P1).

  * Short message: affected services, estimated impact, initial action taken.
* **Status updates**: every 30–60 minutes (P1) or as defined in comms plan.
* **Resolution notice** when service is restored: include root cause (if known), impact summary, user actions (if any).
* **Post-incident report** within 24–72 hours with full RCA and preventive actions.

**Sample initial message (Teams/Email):**

> Subject: [INC-2025-123] Production API - Outage (P1) — Acknowledged
> We are investigating a production API outage affecting all users. Impact: inability to process orders. IT has isolated the affected service and is working on remediation. Next update in 30 minutes. Contact: on-call: +91-XXXXXXXXXX.

---

### Step 7 — Incident Closure & Post-Incident Review

**Who:** Incident owner, IT Manager, relevant stakeholders
**Actions:**

* Confirm all action items completed.
* Close ticket only after verification and stakeholder acceptance.
* Prepare **Post-Incident Report / RCA** (see template below).
* Schedule **Post-Incident Review (PIR)** meeting within 3–7 business days to discuss root cause, corrective actions, and lessons learned.

**RCA template fields:**

```
- Incident ID & Dates (start, detection, resolution)
- Summary & Impact (users, systems, financial impact)
- Root Cause (technical & process)
- Timeline of events & actions taken
- Corrective actions (short & long term)
- Owners & Due dates for each action
- Preventive measures & verification plan
- Approval & Signoff
```

---

## 🧭 Escalation Matrix (Example with Contact Roles)

| Level    |                       Trigger | Escalate To             | Contact Method            |
| -------- | ----------------------------: | ----------------------- | ------------------------- |
| L0       |                   User report | Helpdesk                | Ticket/Phone              |
| L1       |      Unresolved >30min or P2+ | On-call Engineer        | Pager/Phone               |
| L2       |         Unresolved >1hr or P1 | IT Manager / Senior Eng | Call + Incident Channel   |
| L3       | Business-impacting / P1 >2hrs | CTO / Ops Head          | All-hands call, SMS       |
| External |             Vendor dependency | Vendor Support          | Open vendor ticket + call |

---

## 📚 Runbooks & Playbooks (Examples to have ready)

Create concise runbooks for frequent incidents, e.g.:

* **Database failure**: check DB cluster status → promote replica → reconnect app → validate data.
* **Web server outage**: check logs → restart service → check disk space → revert last deployment if needed.
* **DNS outage**: verify DNS provider status → roll back recent changes → update TTL strategies.
* **Backup restore**: verify backup integrity → restore to sandbox → verify → promote to production.

Each runbook should include:

* Prerequisites & permissions required
* Step-by-step commands (with safety checks)
* Rollback steps
* Estimated time to recover (RTO)
* Test verification steps

---

## 🧾 Templates (Copy-Paste Friendly)

### Incident Ticket Template

```
INC-ID:
Title:
Reported By: (Name, Dept, Contact)
Date/Time Detected:
System(s) Affected:
Initial Severity: P1/P2/P3/P4
Number of users impacted:
Short Description:
Attachments (logs/screenshots):
Assigned To:
Status:
Initial Actions Taken:
Next Update ETA:
```

### Emergency Change Form (if rollback/patch required)

```
Emergency Change Request
INC-ID:
Change Description:
Reason for emergency change:
Impact if not applied:
Approver 1 (Name & Signature):
Approver 2 (Name & Signature):
Rollback Plan:
Execution Time:
Post-change verification steps:
```

### Post Incident Report / RCA (summary)

```
INC-ID: 
Start: 
Detect: 
Resolved:
Duration:
Impact: (systems/users/revenue)
Root Cause:
What was done to resolve:
Corrective Actions (who/due date):
Preventive Actions:
Lessons Learned:
Sign-off (IT Manager / CTO):
```

---

## 🛡️ Best Practices (Operational & Security)

**Prevention & preparedness**

* Maintain up-to-date inventory of systems and dependencies.
* Keep a current contact list for team, stakeholders, and vendors.
* Perform regular DR drills and tabletop exercises.
* Apply security patches and critical updates in a timely manner.
* Maintain hot/cold standby or failover for critical services where feasible.

**Detection & monitoring**

* Implement comprehensive monitoring (uptime, performance, logs) with alerting thresholds tuned to avoid alert fatigue.
* Use anomaly detection and SIEM for security incidents.
* Centralize logs (ELK, Splunk, or cloud logging) and keep retention for forensic needs.

**Response & documentation**

* Preserve forensic evidence for security incidents (do not wipe logs).
* Use change records for all emergency modifications and ensure retroactive approvals are recorded.
* Maintain a “lessons learned” registry and ensure corrective actions have owners and deadlines.

**Communication**

* Transparent, timely updates reduce stakeholder anxiety.
* Ensure messages include impact, actions being taken, expected next update, and contact person.

---

## 📈 KPIs & Reporting

Track the following post-incident:

* **MTTD (Mean Time to Detect)** — average time between incident start and detection.
* **MTTR (Mean Time to Recover)** — average time between detection and restoration.
* **Number of P1 incidents per quarter.**
* **Percent of incidents with completed RCA** within 7 days.
* **Percentage of emergency changes with post-hoc change approval**.
* **User satisfaction score** for incident communication (survey).

---

## 🔁 Post-Incident Follow-Up & Continuous Improvement

1. Ensure every corrective action is assigned, with target date and verification criteria.
2. Track remediation tasks in a central project board (Jira / Asana / Trello).
3. Revisit runbooks and monitoring thresholds based on lessons learned.
4. Share a short “incident learnings” summary with all staff (no sensitive details) to improve awareness.

---

## 🧰 Tools & Technologies (suggested)

* **ITSM / Ticketing:** Jira Service Desk, ServiceNow, Zoho Desk
* **Monitoring:** Prometheus, Grafana, Datadog, New Relic
* **Logging / SIEM:** ELK Stack, Splunk, Sumo Logic
* **Communication:** Teams, Slack, Statuspage (public status if customer-facing)
* **Backups / DR:** AWS Backup, Azure Site Recovery, on-prem NAS replication

---
