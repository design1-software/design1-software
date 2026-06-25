# Public and Private Documentation Boundaries

Status: Public-safe governance document  
Purpose: Define what belongs in the public ARIA documentation repository and what must remain private.

## Purpose

This repository exists so ARIA can be documented publicly without exposing application code, private infrastructure, sensitive network details, student information, or operational secrets.

The public documentation should explain ARIA's purpose, learning design, training model, and student experience. It should not reveal how the private environment is deployed, secured, addressed, or administered.

## Public Repository Rule

```text
Public documentation may explain what ARIA teaches and how the learning model works.
Public documentation must not expose how private infrastructure is specifically configured or accessed.
```

## Allowed Public Content

The following content is safe for this repository when written at a high level:

```text
ARIA vision and mission
Training philosophy
Public roadmap summaries
Student experience descriptions
Career progression model
Training domain descriptions
Evidence-based learning standards
Sample tickets with fictional assets
Sanitized runbooks
Sanitized diagrams
Public-facing screenshots with no sensitive details
General technology categories
Instructor governance model
Portfolio-ready examples with fictional data
```

## Content That Must Stay Private

The following content must not be placed in this public repository:

```text
Application source code
Backend route handlers
Authentication/session code
Ticketing integration code
Deployment scripts
Automation scripts that touch infrastructure
Infrastructure-as-code for private systems
Secrets, tokens, keys, passwords, or environment files
Internal IP addresses
Internal hostnames
Private DNS names
Tailnet node names or addresses
Private network topology
Firewall, router, switch, or VPN configuration
Real student names, usernames, emails, or records
Real ticket exports
Private asset inventory
Sensitive screenshots
Logs containing usernames, addresses, tokens, device IDs, or internal paths
Exact production service URLs unless intentionally public
```

## Sanitization Standards

Before publishing documentation, remove or replace:

| Sensitive Item | Public Replacement |
|---|---|
| Internal IP address | `example internal address` or omit entirely |
| Internal hostname | `training workstation` or `domain client` |
| Private domain name | `training domain` |
| Student name | `student` or fictional name |
| Ticket number from real system | fictional ticket number |
| Real device name | `training asset` |
| Real topology | simplified conceptual diagram |
| API route with sensitive operational meaning | high-level workflow description |
| Screenshot with private info | sanitized screenshot or text summary |

## Public Example Standard

Public examples should use fictional values.

Good public example:

```text
Ticket #314: A user reports they cannot log into a training workstation.
The student must verify endpoint identity, account status, network reachability, and policy application.
```

Avoid public examples like:

```text
Ticket #314: User cannot log into a specifically named internal workstation at a specific internal address.
```

## Technology References

It is acceptable to mention broad technology categories, such as:

```text
Active Directory
Linux systems
Windows endpoints
Ticketing systems
AI mentor
Network simulation
Virtual machines
Containers
Security monitoring
Documentation portals
```

Avoid publishing exact private implementation details, such as:

```text
Specific internal addresses
Specific hostnames
Private access URLs
Private credentials
Specific route maps or firewall policies
Exact service tokens or API settings
```

## Documentation Review Checklist

Before adding a file to this repository, confirm:

```text
[ ] No source code is included.
[ ] No secrets or environment values are included.
[ ] No internal IP addresses are included.
[ ] No private hostnames or DNS names are included.
[ ] No real student records are included.
[ ] No real ticket exports are included.
[ ] No private asset inventory is included.
[ ] No sensitive screenshots are included.
[ ] All examples are fictional or sanitized.
[ ] The document explains learning value without exposing operational details.
```

## Relationship to the Private Codebase

The private ARIA codebase remains the operational source of truth for implementation, deployment, automation, integrations, and internal infrastructure.

This public repository is the public documentation layer only.

```text
Private repository: implementation and operations
Public repository: sanitized documentation and learning model
```

## Guiding Principle

ARIA can be public about its mission, learning model, and student outcomes without exposing private operational details.

The public story should be detailed enough to show the quality and seriousness of the platform, but sanitized enough to protect the environment, students, and instructor.
