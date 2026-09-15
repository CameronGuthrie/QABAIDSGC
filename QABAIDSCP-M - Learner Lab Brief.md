# Learner Lab Brief

QABAIDSCP-M | GitHub Copilot Custom Agents

Create a controlled multi-agent workflow for a fictional dependency remediation, implement its automated roles as GitHub Copilot custom agents in VS Code, and test their behaviour. You will submit both the design and evidence of running your profiles.

## Learning outcomes

- Derive roles from required work, then retain, merge, split or remove roles with reasons.
- Turn a role contract into a discoverable `.agent.md` profile with YAML configuration and Markdown instructions.
- Limit tools by responsibility and keep validation separate from production.
- Exercise user-controlled handoffs, missing inputs, rework, escalation and stopping conditions.
- Record evidence and keep consequential decisions with named people.

## Environment and scope

Use current VS Code with GitHub Copilot enabled and an account with access to custom agents in the IDE. Open only the extracted Learner Startpoint folder. Select Workspace when creating profiles so they are saved under `.github/agents/`.

This is a hands-on custom-agent lab. The agents prepare and review Markdown artefacts from simulated evidence. No real application repository, dependency upgrade, test command, security scan or deployment is included. You must label simulation outputs clearly and still record actual Copilot trial behaviour. The local IDE workflow does not require a cloud-agent session or a GitHub issue.

## Scenario

A customer-facing service uses fictional Northstar Parser 4.8.2. Advisory QA-SEC-2026-017 reports a critical vulnerability fixed in 4.9.1 and later supported versions. Version 5.x changes the API. The approved objective is the smallest safe remediation with a complete package for human release review.

Today, interpretation, implementation, review and evidence gathering are poorly coordinated. Reviewers receive incomplete context, rework has no clear owner, and important evidence is repeated or scattered. Your workflow must resolve these problems without assigning release accountability to an agent.

## Acceptance criteria for the imagined remediation

1. The dependency version meets the advisory's fixed-version statement.
2. Public behaviour and published interfaces remain unchanged.
3. The build and automated tests succeed.
4. The scan no longer reports QA-SEC-2026-017.
5. No new High or Critical finding is introduced.
6. The package includes summary, validation evidence, residual risks and rollback information.
7. Uncertainty is visible and no required input is invented.

These criteria guide the simulated review. A simulated PASS cannot establish real release readiness.

## Constraints and human authorities

Keep changes within the approved dependency scope. Do not weaken checks, suppress findings or choose a breaking major upgrade without a Tech Lead decision. Do not deploy. The Security Owner resolves advisory meaning, the Tech Lead owns breaking scope and repeated failure decisions, and the Release Owner records Approve, Revise, Escalate or Stop.

## Required trials

Run BASE plus MISSING-ADVISORY, VERSION-UNAVAILABLE, TEST-FAIL, VULNERABILITY-REMAINS, NEW-HIGH, REPEATED-FAILURE and MISSING-EVIDENCE. Use one fixture case at a time. Preserve actual responses and record the selected profile, tool set, model, expected and observed result, next owner and any retest.

Also demonstrate that profiles appear in the dropdown, handoffs lead to the intended agent without automatic submission, and the validator has no edit tool. A button's appearance is not proof of readiness; a human inspects the output before continuing.

## Completion standard

Every role is justified and implemented, every handoff carries sufficient evidence, and every trial has an observed outcome. Failures route to a named owner and unresolved human decisions stop progression. The profile instructions, design files and trial records must describe the same workflow.

Follow the Stepwise Lab Guide. Compare with the completed example only after producing and testing your own first version.
