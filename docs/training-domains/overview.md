<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/design1-software/design1-software/main/public/ARIA_Logo_dark.png" />
    <img src="https://raw.githubusercontent.com/design1-software/design1-software/main/public/ARIA_Logo.png" alt="ARIA Training Labs" width="200" />
  </picture>
</div>

---

# ARIA Training Domains Overview

Status: Public-safe documentation  
Purpose: Describe ARIA's training areas without exposing private infrastructure details.

## Overview

ARIA organizes practice into **six training domains** that mirror the platform's live lab catalog. The goal is not to teach isolated facts — it is to help students see how help desk, identity, networking, Linux systems, security, and data analysis connect in a real workplace. A single ticket often touches several domains at once.

Across the six domains, ARIA offers **100 hands-on labs** — 95 production-ready and 5 in active development.

| Domain | Focus | Labs |
|--------|-------|------|
| **Help Desk & Ticketing** | Triage, documentation, escalation, professional communication, asset/operations awareness | 24 |
| **Identity & Access Management** | Account review, login triage, group membership, lockouts, MFA, Windows endpoint & policy validation | 21 |
| **Networking & Cisco** | IP/DNS/DHCP, VLANs, routing, switch/router troubleshooting, network automation | 17 |
| **Linux & Systems Administration** | Service status, log review, health checks, safe scripting, automation & documentation | 16 |
| **Security Operations Center** | SIEM alert triage, investigation, incident notes, and an instructor-authorized offensive track | 12 |
| **Data Analysis** | Data profiling & cleaning, star-schema modeling, SQL and pandas analysis, dashboards in Power BI & Tableau, and sensor time-series | 10 |

*(Counts reflect the live catalog; the 5 in-development labs sit within Networking and Security.)*

## Domain 1: Help Desk & Ticketing

Students practice the professional workflow of receiving, triaging, documenting, and escalating support tickets — and the operations awareness that surrounds it, including how real teams track and classify assets.

Skills include:

```text
Reading a ticket carefully
Identifying the affected user or system
Asking clarifying questions
Collecting evidence
Writing professional notes
Avoiding unsupported conclusions
Escalating with useful context
Closing or updating tickets only after review
Asset inventory, ownership, and lifecycle awareness
```

Example public scenario:

```text
A user reports that they cannot access a training workstation.
The student must identify what information is missing, collect safe evidence, and document the next step.
```

## Domain 2: Identity & Access Management

Students practice account and access workflows commonly seen in business environments — including Windows endpoint and policy validation, since most identity issues surface at the endpoint.

Skills include:

```text
User account review
Login issue triage
Group membership concepts
Account lockout workflows
Password policy awareness
Domain membership validation
Multi-factor authentication workflows
Endpoint identity and policy-application checks
Access request documentation and escalation
```

The public documentation describes the concepts only. Private domain names, real accounts, and internal identity configuration are not published here.

## Domain 3: Networking & Cisco

Students practice network troubleshooting from the perspective of endpoints, tickets, and infrastructure evidence — extending into network automation.

Skills include:

```text
IP addressing concepts
Gateway testing
DNS troubleshooting
DHCP review
VLAN awareness
Traceroute/path interpretation
Switch and router troubleshooting concepts
Network automation and repeatable configuration concepts
Network escalation evidence
```

Public documentation does not include private addressing, actual device names, or production topology.

## Domain 4: Linux & Systems Administration

Students practice Linux endpoint and service support workflows, plus the automation and documentation habits that make operations repeatable.

Skills include:

```text
User identity checks
Hostname and system identification
Network path review
Service status review
Disk and memory awareness
Log review concepts
Safe command usage
Checklists, runbooks, and validation notes
Repeatable evidence collection and change summaries
Health check documentation
```

Linux practice supports help desk, systems administration, automation, and security readiness.

## Domain 5: Security Operations Center

Students practice defensive SOC analyst thinking with a path into instructor-authorized offensive exercises.

Skills include:

```text
SIEM alert triage
Failed login investigation
Suspicious process and service analysis
Vulnerability finding review
Web log analysis
Security ticket escalation
Authorized vulnerability scanning
Controlled exploit validation (instructor-authorized only)
Purple team simulation
```

Security practice is designed to be controlled and instructor-governed. The domain runs on a dedicated physical node isolated from production training systems. Offensive exercises require instructor authorization, a written scope statement, isolated targets, and documented teardown.

For the full domain breakdown including the defensive SOC labs and the offensive track, see [security-soc.md](security-soc.md).

## Domain 6: Data Analysis

Students practice turning raw, messy data into trustworthy answers — the analyst workflow of profiling data, cleaning it, modeling it, and reporting findings that hold up to scrutiny. It reinforces the same evidence-first discipline as the rest of ARIA: a conclusion is only as good as the data and the checks behind it.

Skills include:

```text
Data profiling and quality assessment
Cleaning and validating raw datasets
Building fact and dimension tables
Relational (star-schema) data modeling
Analysis with SQL
Analysis with Python (pandas)
Building interactive dashboards in Power BI
Building and publishing dashboards in Tableau
Time-series analysis from sensor data
Documenting assumptions, limitations, and data caveats
Reproducing and explaining a data discrepancy end to end
```

Example public scenario:

```text
A dashboard shows no data for a reporting period.
The student must trace the pipeline, find where records were dropped or mismatched,
correct the model, and document what was wrong and how it was verified.
```

Public documentation describes the analyst concepts and workflow only. Real datasets, private data sources, and internal reporting connections are not published here.

## Capstone

A graduation **Cross-Domain Incident Response capstone** connects the operational domains end to end: a single incident that moves across identity, endpoint, and security operations, requiring the student to investigate, contain, document, and report.

## Cross-Domain and Operational Practice

Real IT work rarely fits into one box, and some practice runs across every domain rather than as a separate track:

- **Asset management & operations** — inventory, classification (training vs. protected), and lifecycle awareness, practiced within help desk and operations work.
- **Outside lab support** — ARIA also tracks outside labs (vendor labs, certification practice, bootcamp exercises, disposable sandboxes): requesting a lab, defining goals, tracking evidence, submitting reflections, and confirming cleanup. Outside labs are non-destructive and instructor-governed.

A single ticket might involve help desk communication, an endpoint check, identity validation, DNS troubleshooting, documentation, and escalation — ARIA is designed to help students see these connections.

## Public Safety Note

This document intentionally avoids private infrastructure details. It does not include internal addresses, private hostnames, device-specific configurations, credentials, or real student/ticket data.
