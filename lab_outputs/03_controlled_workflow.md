# Controlled Workflow

## Happy path

| Step | Owner | Required input | Action | Output / evidence | Receiver | Readiness criteria |
|---|---|---|---|---|---|---|
| 1 | | | | | | |
| 2 | | | | | | |
| 3 | | | | | | |
| 4 | | | | | | |

## Hand-off contracts

For each significant transition, define:

- Sender:
- Receiver:
- Artefact / information:
- Context / assumptions / evidence included:
- Completion criteria:
- Rejection condition:
- Rework or escalation destination:

## Exception and rework paths

| Trigger | Detected by | Immediate action | Named owner of next action | Re-entry / stop condition |
|---|---|---|---|---|
| Missing or contradictory advisory information | | | | |
| Preferred fixed version cannot be used | | | | |
| Tests or compatibility fail | | | | |
| Vulnerability remains after change | | | | |
| New High/Critical finding appears | | | | |
| Repeated validation failure | | | | |

## Human control points

| Decision point | Human owner | Evidence supplied | Allowed decisions | What happens next |
|---|---|---|---|---|
| | | | Approve / Revise / Escalate / Stop | |

## Completion condition

> State exactly what must be true for the workflow to be considered complete.

## Executable Copilot lab sequence

1. Select the coordinator profile with an explicit case ID; save `runs/01_plan.md`.
2. Inspect readiness. If blocked, record the named human route instead of using the next handoff.
3. For a ready plan, select the implementation profile or its handoff; save `runs/02_package.md` with simulated fixture evidence.
4. Select the validation profile with current files attached. It replies in chat; the learner saves `runs/03_validation.md`.
5. For BASE PASS, the learner records the simulated Release Owner decision in `runs/04_human_decision.md`. For failures, follow the named rework/escalation/stop route.
6. Preserve trial results in `runs/05_test_log.md`, then repeat the case matrix from the guide.

Handoffs suggest transitions; they do not validate readiness or record human approval. Case IDs and persisted artefacts carry the evidence. Fresh validation chats provide a useful cross-check but do not guarantee independent reasoning.
