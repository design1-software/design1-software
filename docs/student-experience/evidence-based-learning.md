<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/design1-software/design1-software/main/public/ARIA_Logo_dark.png" />
    <img src="https://raw.githubusercontent.com/design1-software/design1-software/main/public/ARIA_Logo.png" alt="ARIA Training Labs" width="200" />
  </picture>
</div>

---

# Evidence-Based Learning

Status: Public-safe documentation
Purpose: Describe ARIA's evidence standards, proof requirements, and documentation model without exposing private infrastructure.

## What Evidence-Based Learning Means

In most training environments, a student can say "I fixed it" and move on.

ARIA does not accept that.

Evidence-based learning means students are required to **prove what happened** — not describe it, not summarize it, not claim it. Every completed ticket must include real output, real documentation, and a clear record of what was found, what was done, and what the result shows.

The goal is to train students to think and communicate like working IT professionals, not like test-takers.

---

## Proof vs. Claim

ARIA trains students to recognize the difference between a claim and proof.

A **claim** is a statement without support:

```text
The network is down.
I fixed the DNS issue.
The server is healthy.
The user's account is working now.
```

**Proof** is a statement backed by evidence:

```text
A ping from the affected endpoint to the gateway returned no response.
Name resolution from the affected endpoint failed. The configured DNS
server did not return a result for the required internal name.
The service was confirmed active and the process was found running.
The account lockout was cleared and a successful login was documented.
```

Students learn to ask: *What command proves this? What does the output show? What does it not yet prove?*

---

## Discovery vs. Confirmation vs. Proof

ARIA trains students to distinguish between three stages of evidence:

### Discovery
Finding something suspicious or unexpected is not the same as confirming a problem.

```text
A scan returns an open port.
A log shows an unfamiliar entry.
A system check shows an unexpected process.
```

Discovery means: something was found. It does not mean the finding is a breach, a failure, or a root cause.

### Confirmation
Confirming a problem means reproducing or isolating the specific condition.

```text
The open port was confirmed to be associated with an unauthorized service.
The log entry was confirmed to correspond with the time of the reported issue.
The process was confirmed to be consuming abnormal resources.
```

### Proof
Proof means the evidence directly supports the conclusion being stated.

```text
Name resolution was confirmed to fail from the affected endpoint.
The configured DNS server was confirmed to be unreachable from that subnet.
No other endpoints on the same VLAN reported the same behavior.
The evidence supports a DNS configuration issue scoped to this endpoint's network settings.
```

Students are trained to state exactly what their evidence shows — and what it does not yet show.

---

## Scope Enforcement

ARIA validates evidence only from assigned systems.

Students work inside defined lab environments. Evidence collected from systems outside the assigned scope is not accepted. This mirrors real IT environments where technicians are authorized to access specific systems — not the entire infrastructure.

This is not just a safety rule. It is a professional discipline.

A technician who documents findings from unauthorized systems creates liability. ARIA trains students to stay within scope, document their boundaries, and escalate when the investigation requires access they do not have.

---

## Teardown Is Part of the Lab

For temporary lab environments, the lab is not complete when the task is done.

Students must also prove the environment was properly cleaned up.

Teardown evidence may include:

```text
Confirmation that temporary configurations were reversed
Confirmation that test accounts or objects were removed
Confirmation that temporary access was revoked
Confirmation that the lab environment is no longer active
```

A student who completes the task but cannot prove teardown has not completed the lab.

This trains students in a discipline that is critical in real IT environments: **temporary work must be tracked, documented, and reversed**.

---

## Placeholder Evidence Is Blocked

ARIA does not accept placeholder submissions.

The following types of submissions are rejected:

```text
"I ran the command and it worked."
"I checked the system and everything looks fine."
"The issue has been resolved."
"I verified the fix."
```

Students must submit the actual output — the command they ran, the result it returned, and an explanation of what that result proves.

This standard exists because placeholder evidence is a real problem in IT work. A handoff note that says "fixed it" tells the next technician nothing. ARIA trains the habit of documentation that is actually useful.

---

## The Final Note Format

Every completed ticket in ARIA requires a structured final note that follows a professional documentation format:

```text
Symptom
What the user or system reported. What was observed at the start.

Evidence Reviewed
What was checked. What commands were run. What the output showed.

Affected System
Which system or service was confirmed to be involved.

Root Cause
What the evidence shows caused the issue.

Action Taken
What was done to address the root cause.

Verification
What evidence confirms the fix worked or the issue was resolved.

Escalation Decision
Whether the ticket was resolved, escalated, or requires follow-up — and why.
```

This format is not just an ARIA requirement. It mirrors the documentation standard expected in professional IT support, audit environments, and incident response workflows.

A final note written in this format can be understood by the next technician, reviewed by an instructor, included in a student portfolio, and used as a reference if the issue recurs.

---

## What Good Evidence Looks Like

Good evidence is:

```text
Specific — names the exact system, command, or service involved
Timestamped or sequenced — shows when something was checked
Output-based — includes actual command results, not summaries
Scoped — limited to the assigned environment
Honest — reflects what was found, including negative results
```

Negative evidence matters. Documenting that a system was checked and found healthy is as important as documenting a failure. It narrows the problem and shows the troubleshooting sequence was methodical.

---

## Student Outcomes

Students who complete ARIA training with evidence-based standards develop:

```text
The habit of documenting proof before drawing conclusions
The discipline of staying within scope
The skill of writing ticket notes a real team can act on
The judgment to distinguish discovery from confirmation from proof
The professionalism to produce documentation that survives a handoff
```

These outcomes are not just good for ARIA. They are the standard expected in real IT operations environments.

---

## Public Safety Note

This document describes ARIA's evidence standards and learning philosophy at a public level. It does not include private system names, internal addresses, real student work, real ticket data, or specific operational configuration details.
