# Delivery Request: Remediate a Critical Dependency Finding

## Scenario

The engineering team maintains a customer-facing service. A fictional security advisory, **QA-SEC-2026-017**, has identified a critical vulnerability in the service's direct dependency **Northstar Parser**.

The service currently uses Northstar Parser **4.8.2**. The advisory states that the issue is fixed in **4.9.1** and all later supported versions. Version 5.x introduces breaking API changes, so the preferred remediation is the smallest safe upgrade that satisfies the advisory.

The remediation request has already been approved for engineering work. The goal of this lab is **not** to implement the dependency upgrade. The goal is to design that delivery workflow, implement its automated roles as Copilot custom-agent profiles, and exercise the roles against simulated evidence. Actual release readiness remains outside the lab.

## Intended outcome

Produce a controlled multi-agent delivery workflow using GitHub Copilot in VS Code that can take the approved remediation request and produce a **validated, release-ready remediation change**, with explicit ownership, structured hand-offs, controlled rework, and human accountability for consequential decisions.

## Existing process

Today the team generally works like this:

1. A security owner creates a remediation ticket.
2. An engineer interprets the ticket and decides what change is needed.
3. The engineer makes the change and runs tests.
4. A reviewer checks the proposed change.
5. Evidence is gathered manually when the release owner asks for it.
6. The release owner decides whether the change can proceed.

## Known coordination problems

- The remediation ticket does not always translate cleanly into an implementation plan.
- Reviewers sometimes receive a code change without the original acceptance criteria or scan evidence.
- It is unclear who owns rework when validation fails.
- The same evidence can be checked repeatedly by different people.
- A release decision can be delayed because evidence is incomplete or spread across several places.
- Nobody wants an AI agent to silently waive a security requirement, suppress a failed check, or approve the release itself.
