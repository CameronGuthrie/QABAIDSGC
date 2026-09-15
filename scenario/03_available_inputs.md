# Available Inputs

Treat the following as the authoritative input set for the lab:

- `01_delivery_request.md` — the approved remediation request and current-process problems.
- `02_acceptance_criteria_and_constraints.md` — success criteria, constraints, human authorities and exception conditions.

No application source-code repository is required for this exercise. You must create and run Copilot custom-agent profiles in the local VS Code workspace. Where an implementation agent would normally produce code, tests or scan output, model those items as **delivery artefacts and evidence** in the workflow.

- `04_simulated_evidence.md` supplies fictional evidence and isolated trial cases. Select one case per run; its overrides apply only to that trial.

The lab uses real Copilot profile execution to prepare and review simulated Markdown artefacts. Do not claim that the profiles performed a real dependency upgrade or generated the fixture evidence.

## Important design rule

Do not begin by choosing a number of agents. Begin with the outcome and required work, then let the structure of the workflow determine which responsibilities should become agent roles and which decisions should remain human-owned.
