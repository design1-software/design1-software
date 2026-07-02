<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/design1-software/design1-software/main/public/ARIA_Logo_dark.png" />
    <img src="https://raw.githubusercontent.com/design1-software/design1-software/main/public/ARIA_Logo.png" alt="ARIA Training Labs" width="200" />
  </picture>
</div>

---

# ARIA Mentor

Status: Public-safe documentation
Purpose: Describe the ARIA AI Mentor's coaching model and validation mechanics without exposing private implementation details.

## What the ARIA Mentor Is

The ARIA Mentor is the AI coaching layer inside the ARIA platform.

It is not a search engine. It is not a helpdesk bot. It is not a tool that hands students the answer when they are stuck.

The ARIA Mentor is designed to behave like a **senior teammate who is invested in your growth** — someone who will ask the right questions, push back on weak evidence, and make you prove your work before moving forward.

The goal is to build judgment and professional discipline, not to create dependency.

---

## What the Mentor Does Not Do

The ARIA Mentor is explicitly designed to avoid certain behaviors that undermine learning:

```text
It does not give away the answer when a student is stuck.
It does not accept vague claims in place of real evidence.
It does not let students skip documentation steps.
It does not validate work that was done outside the assigned scope.
It does not approve submissions that are missing required evidence.
```

The mentor's job is to make the student prove their work — not to make the lab easier to finish.

---

## The Coaching Approach

When a student is working a ticket, the ARIA Mentor guides through questions, not answers.

Instead of telling a student what to check, the mentor asks:

```text
Which system are you currently inside? How do you know?
What does your before-state evidence show?
What command proves the issue exists?
Which component is wrong — and what is the proof?
What does the output show? What does it not yet prove?
What command confirms the fix worked?
What does your after-state evidence show?
Is this ready for instructor review, or is something still missing?
```

This approach trains students in the thinking pattern of experienced IT professionals: identify the system, gather evidence, isolate the cause, apply a scoped fix, verify the result, document the work.

---

## Four Core Mechanics

### 1. Template-Aware Validation

For each lab ticket, the ARIA Mentor loads the template associated with that specific assignment.

The template defines what evidence is required before the ticket can be submitted for instructor review. Required fields typically include:

```text
Before-state evidence — what was observed before any action was taken
Root cause statement — what the evidence shows caused the issue
Fix documentation — what action was taken and why
After-state evidence — what was observed after the fix was applied
Final note — a structured summary written in professional IT format
```

The mentor checks each submission against these required fields and notifies the student of anything missing before the work moves forward.

### 2. Placeholder Evidence Blocked

The ARIA Mentor does not accept placeholder submissions.

A student cannot submit:

```text
"I ran the ping and it worked."
"I checked the service and it looked fine."
"Everything is resolved now."
```

These statements describe outcomes without providing evidence. The mentor requires the actual command output — what was run, what it returned, and what that result proves.

This is not a technicality. It is the core professional standard ARIA is training. A ticket note that says "fixed it" is not useful to the next technician, the instructor reviewing the work, or the student building a portfolio.

### 3. Instructor Always in the Loop

The ARIA Mentor does not close tickets or update the ticketing system on its own.

After a student's evidence passes validation, the work is queued for instructor review. The instructor must approve the submission before the final resolution note is written to the ticket as the official record.

This single-approval, one-time writeback model mirrors how real IT environments work: AI and automation may assist, but a human professional remains accountable for the official record.

The instructor can:

```text
Approve the submission and allow the ticket to close
Request additional evidence before approving
Add feedback on documentation quality or troubleshooting sequence
Flag the work for follow-up or remediation
```

### 4. Portfolio-Ready Documentation

Every lab produces a structured final note written by the student and approved by the instructor.

The format is designed to be professional and reusable:

```text
Symptom          — what was reported or observed
Evidence         — what was checked and what it showed
Root Cause       — what the evidence identified as the cause
Action Taken     — what was done to address it
Verification     — proof that the fix worked
Escalation       — whether the ticket was resolved, escalated, or needs follow-up
```

These notes are written in professional IT support language. They are suitable for inclusion in a student evidence portfolio, for use as handoff documentation, and as examples of the student's documentation standard.

---

## What the Mentor Teaches

Through consistent coaching across many tickets, the ARIA Mentor trains students to:

```text
Identify which system they are on and why that matters
Gather evidence before drawing conclusions
State exactly what evidence shows and what it does not yet show
Distinguish discovery from confirmation from proof
Document work that can be understood by the next person
Recognize when a problem is out of scope or requires escalation
```

These are not abstract skills. They are the habits that distinguish a technician who can work independently from one who still needs constant direction.

---

## Relationship to the Instructor

The ARIA Mentor handles coaching, validation, and documentation guidance.

The instructor handles progression, approval, feedback, and final authority over all lab outcomes.

The mentor does not replace the instructor. It ensures that by the time a submission reaches the instructor, the evidence is real, the documentation is structured, and the student has already answered the basic questions the instructor would ask.

This frees instructor time for the work that matters most: reviewing thinking quality, providing targeted feedback, and making progression decisions based on demonstrated readiness.

---

## Public Safety Note

This document describes the ARIA Mentor's coaching model and validation approach at a public level. It does not include private system configurations, internal implementation details, API structures, prompt engineering, or backend logic.
