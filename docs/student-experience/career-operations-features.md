<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/design1-software/design1-software/main/public/ARIA_Logo_dark.png" />
    <img src="https://raw.githubusercontent.com/design1-software/design1-software/main/public/ARIA_Logo.png" alt="ARIA Training Labs" width="200" />
  </picture>
</div>

---

# Career Operations Features

Status: Public-safe documentation
Purpose: Describe the full set of Career Operations features inside ARIA without exposing private implementation details.

## Overview

Career Operations Mode is more than a ticket queue. It is a full enterprise training environment built around how IT professionals actually work — with levels, assignments, onboarding workflows, shift structure, lab access, and a dashboard that keeps everything visible.

This document describes the six features that make up the Career Operations experience.

For the core Career Operations Mode overview, see [career-operations-mode.md](career-operations-mode.md).
For the daily ticket queue experience, see [shift-mode.md](shift-mode.md).

---

## Feature 1: Career Progression

Students move through defined career levels with instructor-approved promotions.

Each level unlocks specific practice areas, ticket types, and lab access. Students cannot access work that is above their current level by default. Progression is not automatic — it requires demonstrated readiness through completed tickets, evidence quality, documentation quality, and safe behavior.

```text
L1 / L2  — Junior IT Operations
L3 / L4  — Intermediate Infrastructure Operations
L5+      — Senior Operations / Engineering
```

Instructors control all promotion decisions. A student who is ready can be promoted. A student who has completed ticket volume but is not yet demonstrating documentation quality or safe behavior is not promoted until those standards are met.

For detailed level descriptions, see [career-operations-mode.md](career-operations-mode.md).

---

## Feature 2: Shift Mode

Students start and end shifts like a real enterprise workday.

At the beginning of a shift, students see a queue of available work filtered to their current level, approved practice areas, and active assignments. They choose a ticket, work it, submit evidence, and move to the next.

This structure teaches prioritization and professional rhythm — not just technical skills.

For the full Shift Mode description, see [shift-mode.md](shift-mode.md).

---

## Feature 3: Assignment Bridge

Before a ticket assignment is created, ARIA validates that the work matches the student's career level and approved asset tier.

This means students are not handed work they are not ready for, and instructors do not need to manually verify every assignment against a student's current status. The system checks the match before the assignment exists.

The assignment bridge connects:

```text
Student career level → appropriate ticket type
Approved practice areas → eligible lab targets
Asset classification → permitted scope of work
```

If a student's level or approved areas do not match the intended assignment, the assignment is not created. The instructor can override this when assigning stretch work intentionally.

---

## Feature 4: Employee Onboarding Practice

Students can practice the full workflow of onboarding into a new environment — a common real-world scenario that most IT training programs never simulate.

Employee onboarding practice in ARIA includes:

```text
Reviewing onboarding requirements before beginning
Following a structured checklist
Collecting evidence at each onboarding step
Producing a professional onboarding packet for instructor review
```

This trains students in a workflow they will encounter in their first real IT role. Many new hires know how to configure systems but have never practiced the documentation and process discipline that professional onboarding requires.

The instructor reviews the onboarding packet and approves or requests corrections before the practice is marked complete.

---

## Feature 5: Student Operations Dashboard

Each student has a single-page dashboard that shows their current status across all active work.

The dashboard is designed to give a student everything they need to begin a shift without asking the instructor what to do next.

Dashboard elements include:

```text
Current career level
Active shift status
Assigned tickets and their current stage
Eligible practice areas based on current level
Active lab assignments and reference information
Next steps toward promotion
Instructor notes and feedback
```

The dashboard reflects the way real IT professionals track their own workload — not through a list of lessons, but through a live view of what is assigned, what is in progress, what is waiting for review, and what needs to be done next.

---

## Feature 6: Outside Lab Support

ARIA supports a structured workflow for outside lab practice — including CTF-style challenges, certification preparation exercises, vendor labs, and other environments that exist outside the core ARIA infrastructure.

Outside lab support is not unstructured. It follows a defined lifecycle:

```text
Request          — student submits a request describing the lab and its learning goals
Approval         — instructor approves the request and any scope boundaries
Active Use       — student completes the lab and tracks evidence
Documented Teardown — student documents that the environment was cleaned up or destroyed
Verified Destruction — instructor confirms the teardown evidence is sufficient
```

This workflow matters for two reasons.

First, it keeps outside labs accountable. A lab that was never documented was never really done. A lab environment that was never confirmed destroyed is a liability.

Second, it prepares students for how real IT teams handle temporary infrastructure — with approval, tracking, and formal closure, not informal access that goes unrecorded.

---

## How These Features Work Together

Career Operations is designed so that each feature reinforces the others.

A student at the start of a session:

```text
1. Opens the Student Operations Dashboard
2. Sees their current level, active assignments, and shift status
3. Begins a shift through Shift Mode
4. Picks up a ticket that was matched to their level via Assignment Bridge
5. Works the ticket with ARIA Mentor coaching and evidence validation
6. Submits for instructor review
7. Checks promotion progress or outside lab status while waiting
```

The system is designed to feel like arriving for a real shift — not like logging into a course platform.

---

## Public Safety Note

This document describes the Career Operations feature set at a public level. It does not include private system names, internal addresses, backend architecture, real student records, or specific operational configuration details.
