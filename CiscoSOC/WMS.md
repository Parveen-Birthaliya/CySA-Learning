# Definition of WMS (Workflow Management System)

## What is a WMS?

A **Workflow Management System (WMS)** is a software platform designed to:

- **Tag and identify** existing security events
- **Track** the event lifecycle from detection to closure
- **Log and manage** actions taken during:
  - Detection
  - Response
  - Mitigation
  - Ticket resolution

---

## Role of WMS in Security Operations

A WMS functions as a **platform for orchestrating and automating incident response workflows**.

### In simpler terms:
> 🔁A **WMS automates the remediation** of a malicious action. It facilitates **containment** and **eradication**.

However, it is important to understand what a WMS **does not do**:
- ❌ **Does not detect incidents**  
- ❌ **Does not collect evidence**  
- ❌ **Does not handle approvals**

Those responsibilities lie with systems such as:
- **SIEM**: for detection and evidence collection
- **Ticketing Systems**: for workflow and approval tracking

---

## WMS Workflow in a SOC Context

### Typical Flow:
1. **SIEM** identifies an incident and generates an alert.
2. A **Tier 1 Analyst** collects initial evidence.
3. A **Tier 2 or Tier 3 Analyst** confirms the incident.
4. The **WMS** is triggered to:
   - Automate response playbooks
   - Orchestrate remediation actions
   - Interface with security infrastructure (firewalls, EDR, etc.)

---

## Key Capabilities of a WMS

| Capability                 | Description                                                                 |
|---------------------------|-----------------------------------------------------------------------------|
| **Automation**            | Executes incident response tasks without human intervention                |
| **Orchestration**         | Coordinates actions across multiple security tools                         |
| **Containment & Eradication** | Executes isolation, quarantine, or removal actions on affected assets      |
| **Ticket Lifecycle Management** | Ensures end-to-end visibility and closure of incident workflows          |

