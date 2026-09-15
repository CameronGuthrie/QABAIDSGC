# Role Contracts

Duplicate the contract below for every final agent role.

---

## Agent: <name>

### Purpose
One sentence describing the agent's unique contribution to the delivery outcome.

### Responsibilities
- 
- 

### Required inputs
- 
- 

### Outputs and quality criteria
- Output:
- Required structure / evidence:
- Completion criteria:

### Boundaries / prohibited actions
- 
- 

### Hand-offs
- Sends to:
- Artefact / information transferred:
- Readiness criteria:

### Clarification, rejection and escalation
- Missing input:
- Failed quality criteria:
- Escalation condition:

---

## Copilot implementation mapping

Map every design role to its `.github/agents/<name>.agent.md` file. Record description, enabled tools, required sources, output ownership and handoff target. The completed example uses `remediation-coordinator`, `change-implementation` and `independent-validation`. The validator has read/search only; the other two also have edit. No role enables execution tools.

In this lab, implementation and validation operate on simulated evidence. Validation replies in chat and the learner saves its report. The learner owns the human decision record. The underlying production design still requires real independently reviewed build/test/scan evidence before a real release.
