<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/design1-software/design1-software/main/public/ARIA_Logo_dark.png" />
    <img src="https://raw.githubusercontent.com/design1-software/design1-software/main/public/ARIA_Logo.png" alt="ARIA Training Labs" width="200" />
  </picture>
</div>

---

# Security and SOC Domain

Status: Public-safe documentation — Active Build
Purpose: Describe the Security and SOC training domain without exposing private infrastructure, internal hostnames, or operational configuration.

## Domain Philosophy

The Security and SOC domain is designed around one principle: **defensive-first, offensive-available**.

The primary path is junior SOC analyst thinking. Students learn to read alerts, investigate anomalies, analyze logs, distinguish evidence from assumption, and write professional incident documentation. The offensive track is available as a controlled extension — not a shortcut, not a default, and never unscoped.

The ARIA evidence standard applies throughout both paths:

```text
Every command needs a stated purpose.
Every screenshot needs to answer: what does this prove?
Never claim more than the evidence supports.
```

---

## What the Domain Teaches

### Defensive Path

Students in the defensive SOC path learn to work like junior SOC analysts:

```text
Read and triage SIEM alerts
Investigate failed logins, suspicious processes, and vulnerability findings
Analyze Linux authentication logs
Analyze Windows event logs
Analyze web access logs, firewall logs, SSH logs, and DNS logs
Distinguish discovery from confirmation from proof
Write SOC-style ticket updates
Write professional escalation notes
```

The distinction between discovery, confirmation, and proof is central to this domain. A log entry showing a failed login is discovery. Confirming the account, source, and pattern is confirmation. Proving the activity represents a specific threat requires additional evidence. Students are trained to state exactly what each piece of evidence shows — and what it does not yet show.

### Offensive Track

Offensive exercises are available as a controlled, instructor-authorized extension of the security domain.

These are not unstructured hacking exercises. Every offensive lab requires:

```text
Instructor approval before any activity begins
A defined scope statement identifying the authorized targets
Isolated targets — separated from production training systems and the physical network
Documented teardown evidence at the conclusion of every lab
```

The ARIA Mentor applies the same four-layer standard to offensive work: what was done, why, what does it prove, and what is the next step.

---

## The Dedicated Security Node

The Security and SOC domain runs on a dedicated physical server separate from ARIA's primary training infrastructure.

This isolation is intentional. Security lab activity — including offensive exercises — cannot affect student daily-use systems, production training services, or the physical network. The security node hosts:

```text
The SIEM stack (manager, indexer, and dashboard)
Dedicated student Windows training VMs
An isolated security-training Active Directory domain
An offline offensive lab range for authorized exercises
A NAS layer for VM backups, student artifacts, and portfolio archives
```

The security node is designed to eventually join ARIA's primary infrastructure as a clustered node while maintaining its isolation boundaries for offensive work.

---

## Six Defensive SOC Labs

### SEC-001 — Wazuh Alert Triage

**Scenario:** A SIEM alert fires on a training endpoint. The student must identify the alert, classify it, and write a professional SOC disposition note.

**Evidence Required:**
```text
Alert details — rule ID, severity level, affected host, timestamp
Student explanation of what the alert indicates
Classification decision — benign, suspicious, or escalate
Final SOC note in professional format
```

**What This Teaches:** Reading a SIEM alert is not the same as understanding it. Students practice identifying exactly what the rule fired on, why it fired, and whether the activity warrants investigation or closure.

---

### SEC-002 — Failed Login Investigation

**Scenario:** Multiple failed login alerts are generated against a training endpoint or account. The student must investigate the source, pattern, and account involved, and determine whether to escalate.

**Evidence Required:**
```text
Alert or log output showing the failed attempts
Affected account name
Source identification
Attempt pattern — count, time range, distribution
Local log confirmation of the activity
Final incident note with escalation decision and reasoning
```

**What This Teaches:** Failed logins are one of the most common alert types in real SOC environments. Students practice distinguishing a user lockout from a brute force pattern from a misconfigured service — using evidence, not assumption.

---

### SEC-003 — Suspicious Process or Service

**Scenario:** A SIEM alert or manual review surfaces an unexpected process or service running on a training endpoint. The student must identify the process, assess it, and document their findings.

**Evidence Required:**
```text
Alert details or review output
Host identity confirmation
Process or service name and command line
User context — which account is running it
Student explanation of what the evidence proves
Assessment — benign, suspicious, or escalate
```

**What This Teaches:** Not every unexpected process is a threat. Students practice identifying processes, understanding user context, and making evidence-based assessments rather than reflexive escalations.

---

### SEC-004 — Vulnerability Finding Review

**Scenario:** A vulnerability scan or package audit surfaces an outdated component on a training system. The student must review the finding, assess the severity, and document a remediation recommendation.

**Evidence Required:**
```text
Finding details — tool output or scan result
Affected host
Component name and current version
Severity classification or CVE reference
Explanation of the version-vs-exploitation distinction
Recommended remediation action
```

**What This Teaches:** Finding a vulnerable version is not the same as confirming exploitation. Students practice stating exactly what a finding proves — and where the evidence ends.

---

### SEC-005 — Web Log Suspicious Activity

**Scenario:** A review of web access logs surfaces a suspicious request pattern from a specific source. The student must analyze the pattern, document the activity, and make an escalation decision.

**Evidence Required:**
```text
Log excerpts showing the relevant requests
Source IP identification
Request paths and user agent strings
Status code patterns
Student explanation of what the pattern indicates
Escalation decision with reasoning
```

**What This Teaches:** Log analysis is a core SOC skill. Students practice reading raw logs, recognizing patterns, and translating what they see into a structured finding that a senior analyst can act on.

---

### SEC-006 — Security Ticket Escalation Drill

**Scenario:** A student receives a partially documented security ticket that is missing evidence needed to escalate properly. The student must identify what is known, identify what is missing, and write a professional escalation note requesting the specific evidence needed.

**Evidence Required:**
```text
Summary of known facts from the existing ticket
List of what evidence is missing and why it matters
Specific request for the next evidence needed
Escalation note written in professional SOC format
Explanation of escalation reasoning
```

**What This Teaches:** In real SOC environments, students will often inherit incomplete tickets. Knowing how to work with partial evidence — and how to clearly request what is missing — is as important as investigating from scratch.

---

## Minimum Viable Production

The Security and SOC domain is considered production-ready when the following are in place:

```text
SEC-001 through SEC-003 lab templates active
At least one Linux agent endpoint online
At least one Windows agent endpoint online
SIEM alerts confirmed firing on controlled test events
ARIA Mentor validation active for SEC-domain submissions
Instructor review queue connected for SOC lab submissions
```

SEC-004 through SEC-006 expand coverage and will be added as the domain matures.

---

## Offensive Lab Track

The offensive track is a controlled extension available to students who have demonstrated readiness in the defensive SOC path and received explicit instructor authorization.

### Lab Types

| Type | Description |
|------|-------------|
| Authorized Vulnerability Scanning | Full-port scans and service enumeration against isolated training targets |
| Controlled Exploit Validation | Instructor-staged vulnerable environments; student identifies and validates exploits with scoped access |
| Disposable CTF-Style Exercises | Isolated vulnerable systems designed for exploitation practice in a contained range |
| Purple Team Simulation | Instructor stages an attack scenario; student plays analyst or incident responder |

### Hard Rules

These rules are not guidelines. They are enforced requirements for every offensive lab activity.

```text
Instructor approval and a written scope statement are required before any offensive activity begins.

All targets operate on an isolated network segment — not connected to the physical LAN,
production ARIA services, or any systems outside the authorized range.

No scanning, testing, or enumeration against public systems, real infrastructure,
or ARIA training services under any circumstances.

Teardown evidence is required as the final submission step.
Students must prove the lab environment is destroyed or returned to baseline.

The ARIA Mentor applies the same evidence standard to offensive work:
every action needs a stated purpose, and every finding needs documented proof.
```

### Why These Rules Exist

Offensive security training without scope enforcement is not training — it is liability.

ARIA's offensive track is designed to prepare students for authorized penetration testing, red team exercises, and vulnerability validation work in professional environments. Those environments require scope statements, authorization records, and teardown documentation. ARIA teaches those habits from the first offensive lab.

---

## Evidence Standard for Security Work

The ARIA evidence standard applies to all security labs — defensive and offensive.

Students are not allowed to:

```text
Claim a system is vulnerable without showing the version and finding
Claim a scan found something without providing the output
Claim a process is suspicious without documenting what makes it suspicious
Claim an exploit worked without showing the before and after state
Claim teardown is complete without providing evidence the environment is gone
```

The same format applies to all security ticket submissions:

```text
Symptom or Alert — what was observed or triggered
Evidence Reviewed — what was checked and what it showed
Affected System — which host or account is involved
Root Cause or Finding — what the evidence identifies
Action Taken — what was done in response
Verification — proof the response was effective or the finding was confirmed
Escalation Decision — whether the ticket is closed, escalated, or pending more evidence
```

---

## Public Safety Note

This document describes the Security and SOC domain at a public level. It does not include internal hostnames, private domain names, internal IP addresses, Tailscale configuration, SIEM admin credentials, specific VM inventory, or offensive range network details. All lab scenarios reference training environments only. No real student data, real alert exports, or production system configurations are published here.
