<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/design1-software/design1-software/main/public/ARIA_Logo_dark.png" />
    <img src="https://raw.githubusercontent.com/design1-software/design1-software/main/public/ARIA_Logo.png" alt="ARIA Training Labs" width="200" />
  </picture>
</div>

---

# Access Model — Any Device, Anywhere

Status: Public-safe documentation
Purpose: Describe how students reach their labs, at a high level, without exposing private infrastructure, addresses, or access URLs.

## The Idea

ARIA is delivered entirely in the browser. There is **nothing to install, no VPN, and no client** to configure. A student can start a shift from a laptop, a Chromebook, a borrowed library computer, or a phone — and get the same workspace every time.

This is deliberate. Real IT professionals log in from wherever they are and get to work. ARIA students practice inside that same expectation from their first day, instead of fighting a setup process before they can learn anything.

## Signing In

The sign-in flow is simple on the surface and strict underneath:

```text
1. Open ARIA in any web browser.
2. Enter your email — a one-time code is sent to it.
3. Type the code. That's it — you're verified.
4. You land on a personal workspace showing only the lab systems assigned to you.
```

There is **no shared password to leak and nothing to memorize.** Identity is proven by control of the student's own email inbox, one session at a time.

## What a Student Sees

Once signed in, each student sees only their own resources — never another student's, and never the wider environment:

- **A Linux workspace** — a full terminal, streamed to the browser, that opens already logged in.
- **A Windows workspace** — a complete desktop for identity, policy, and endpoint labs, streamed the same way.
- **Additional lab systems** — network simulation, identity/MFA tooling, and similar resources are made available by the instructor when a lab calls for them.

Everything renders as pixels in the browser tab. The student's own device never joins the private network and never needs special software.

## How It Stays Safe (High Level)

Behind that simple experience is a **zero-trust, least-privilege** access model:

- An **identity-aware access gateway** verifies every student at the edge before any lab system is reachable. Unauthenticated requests never touch the environment.
- A **browser-based access broker** then connects the verified student to only the specific resources assigned to them — one student, one set of tiles.
- The **student path and the instructor/management path are completely separate.** Students never receive direct network access; the instructor administers the environment over an entirely different, private channel.
- Nothing lab-facing is exposed directly to the open internet.

The outcome is enterprise-grade access control that a first-week student can use without a setup call — while the underlying network, addresses, and administration remain private.

## What This Document Does Not Include

Consistent with ARIA's [public/private boundaries](../governance/public-private-boundaries.md), this document intentionally omits internal addresses, private hostnames, tailnet details, exact access URLs, container or VM identifiers, and any configuration specifics. It describes the *student experience and the security model*, not the deployment.
