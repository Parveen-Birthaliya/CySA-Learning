# SOC Workflow for an Alert

This document outlines a standardized workflow for handling alerts within a Security Operations Center (SOC), progressing from Tier 1 triage to incident resolution and management reporting.

---

## 🔹 Tier 1 SOC Analyst – Initial Alert Triage

Triggered upon SIEM alert reception:

1. **Open case** in the ticketing system.
2. **Lookup user details** (name, location, email, manager) from the user directory.
3. **Resolve hostname and IP address** for the user.
4. **Query threat intel platform** using IP address:
   - Determine threat source
   - Review related threats
   - Evaluate reputation score
5. **Collect proxy traffic logs** and attach to the case.
6. **Collect packet captures (PCAPs)** for further review.
7. **Analyze user traffic history** in conjunction with threat intel.
8. **Assign severity and priority** based on contextual analysis.
9. **Escalate case to Tier 2** for advanced investigation.

> **Note:** Tasks like contextual analysis of traffic and severity assignment typically require manual review.

---

## 🔹 Tier 2 SOC Analyst – Deep Dive Investigation

Activated post-escalation from Tier 1:

1. **Review threat intelligence** and case history.
2. **Analyze packet captures** to detect potential exploits.
3. **Query endpoint systems** for indicators of compromise (IOCs).
4. **Collect endpoint logs** and memory dumps.
5. **Evaluate need for containment** based on impact analysis.
6. **Execute containment** actions (isolate, block, kill).
7. **Add artifacts and evidence** to the ticket.
8. **Notify Tier 3 and management** for further handling.

---

## 🔹 Tier 3 / Incident Handler – Remediation & Threat Intelligence

Engaged for confirmed or high-severity incidents:

1. **Deploy technical support** to:
   - Reimage infected machine
   - Extract malware or suspicious binaries
2. **Extract new IOCs** and send to threat intel platform.
3. **Draft threat summary and context report**.
4. **Update and close** the incident ticket.

---

## 🔹 Management – Metrics and Oversight

Post-incident activities:

- **Compile incident metrics**:
  - Time to Detect (TTD)
  - Time to Contain (TTC)
  - Time to Resolve (TTR)
  - Time to Close (TTCL)
- **Analyze incident response performance**.
- **Drive continuous improvement and SLA compliance**.

---

## Summary Table

| **SOC Role**       | **Primary Functions**                                                        |
|--------------------|-------------------------------------------------------------------------------|
| Tier 1 Analyst     | Alert triage, enrichment, contextual review, severity assignment, escalation |
| Tier 2 Analyst     | Packet/endpoint analysis, containment, forensic evidence gathering           |
| Tier 3 / IR Team   | System remediation, malware analysis, IOC extraction                         |
| Management         | Reporting, SLA metrics, performance improvement                              |

