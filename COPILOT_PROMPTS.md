# Copilot custom agent prompt sequence

Course QABAIDSGC-M. These are inputs to try, not recorded Copilot outputs. Use an explicit selected profile at each stage. Attach the required files with Add Context or the # picker, and inspect changes before accepting them.

## Design before creating profiles

Use the default Copilot assistant to analyse `scenario/01_delivery_request.md` and `scenario/02_acceptance_criteria_and_constraints.md`: identify outcome, required work, dependencies, evidence, exceptions and human decisions before naming agents. Draft roles, then challenge overlap, gaps, unnecessary handoffs and self-approval. Record Retain, Merge, Split or Remove decisions in `lab_outputs/01_agent_team_design.md`.

Ask for role contracts and a workflow, then review them yourself. Save contracts and workflow in the corresponding `lab_outputs/` files. Do not copy the completed example before defending your own structure.

## Create each profile

Use the IDE custom-agent creation flow described in the guide. With one role contract attached, ask Copilot: "Draft the YAML frontmatter and instructions for this role as a VS Code custom agent. Use an explicit description, target: vscode, least required tools and case-specific input/output contracts. Enable no terminal, web, MCP or subagent tools. Do not add a model name. Include missing-input behaviour and human escalation. The validation role must have read/search only."

Review the draft, save it in `.github/agents/<role>.agent.md`, and verify the profile in the dropdown. Add any handoffs only after the target profile exists.

## Run the coordinator

Select your coordinator. Example profile name: `remediation-coordinator`.

"Case BASE. Read the scenario and selected fixture. Create a simulated remediation plan and evidence checklist in lab_outputs/runs/01_plan.md. Map all seven acceptance criteria, name human authorities, and state READY or NOT READY with reasons. Do not create the package."

## Run the package role

Select your implementation profile or use the coordinator handoff. Example: `change-implementation`. Review the prefilled prompt before submitting.

"Case BASE. Read the saved plan and selected fixture. If the plan is ready, create lab_outputs/runs/02_package.md using the supplied simulated evidence. Include summary, rollback and residual risk. Do not claim to run tests or approve readiness."

## Run the validator

Select your validation profile. Example: `independent-validation`. Attach the plan, package and selected fixture; for an additional challenge, use a fresh chat.

"Case BASE. Validate the saved plan and package against every acceptance criterion and the selected fixture facts. Reply in chat with a Markdown report, outcome, evidence, next owner and re-entry condition. Do not change any files or decide release."

Save the response yourself in `lab_outputs/runs/03_validation.md`. Complete the human decision record yourself and log the observation.

## Trial the exceptions

Preserve the previous trial before creating case-specific outputs. Replace BASE with each case ID from `scenario/04_simulated_evidence.md`. Start MISSING-ADVISORY and VERSION-UNAVAILABLE at the coordinator and verify it pauses. Run TEST-FAIL, VULNERABILITY-REMAINS, NEW-HIGH, REPEATED-FAILURE and MISSING-EVIDENCE through the ready-plan/package/validation path. Attach the selected case's prior failure fact for REPEATED-FAILURE.

Use: "Case <CASE-ID>. Apply only this case's overrides. Do not use expected-result labels as evidence. Show the applicable facts, outcome, next owner and required action."

Record the actual response, compare it with the expected route, and fix/retest the profile if it fails. A trial does not pass just because the expected answer is printed in the fixture.
