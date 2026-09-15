---
name: replace-with-role-name
description: Replace with one clear purpose and capability statement.
target: vscode
tools: ['read', 'search']
user-invocable: true
disable-model-invocation: true
---

# Role instructions

This is an incomplete scaffold. Save a completed copy as `.github/agents/<role-name>.agent.md` after using the Workspace custom-agent creation flow. Do not put this template into the discovery folder unchanged.

## Purpose and responsibility

TODO: Define one purpose and the work owned by the role.

## Required inputs

TODO: List authoritative scenario files, selected case ID, upstream artefacts and any human decision. State what happens if they are missing or contradictory.

## Outputs and quality criteria

TODO: Define the output path or chat report, fields, evidence mapping and readiness criteria. Label fixture-derived work SIMULATED.

## Tools and boundaries

TODO: Keep only tools needed by this role. Add edit only to roles that must write artefacts. Do not enable terminal, web, MCP or subagent tools for this lab. The validator must remain read-only. Define file ownership; tool lists do not restrict edits to a path.

## Handoff and exceptions

TODO: Name the receiver, artefact, readiness check, failure route and human escalation. Optionally add a VS Code handoff with label, agent, prompt and send: false after the target profile exists. Explain that a button is not a readiness gate.
