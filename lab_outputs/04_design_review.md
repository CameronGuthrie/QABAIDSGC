# Design Review

Use this sheet before treating the design as complete.

## Coverage
- [ ] Every required workflow step has a clear owner.
- [ ] No required responsibility falls between roles.
- [ ] Every agent has a necessary and distinct primary purpose.

## Role quality
- [ ] No role is a vague do-everything assistant.
- [ ] No agent both produces work and independently approves its own output where independence matters.
- [ ] Boundaries identify decisions/actions outside each agent's authority.

## Hand-offs
- [ ] Every important hand-off names sender and receiver.
- [ ] The transferred artefact/evidence is explicit.
- [ ] Readiness/completion criteria are explicit.
- [ ] Rejection and escalation routes are explicit.

## Exceptions and control
- [ ] Missing required inputs cause clarification or escalation, not guesswork.
- [ ] Failed validation returns work to a named owner.
- [ ] Repeated failure has an escalation or stopping condition.
- [ ] Human decisions are visible wherever judgement or accountability matters.

## Simplicity
- [ ] Every interface adds useful specialisation, independence or control.
- [ ] Removing an agent/interface would reduce reliability, clarity or control.

## Final challenge

What is the weakest boundary or hand-off in your design, and what evidence would show that it needs to change?

## Copilot acceptance checks

- [ ] Every chosen automated role has a discovered `.agent.md` profile.
- [ ] Each description, tool set and instruction body matches its role contract.
- [ ] The validator cannot edit files through its configured tools.
- [ ] Handoff targets resolve and prompts wait for manual submission.
- [ ] Blocked plans do not proceed solely because a handoff button is visible.
- [ ] BASE and every exception case have an observed result, evidence and next owner in the test log.
- [ ] No fixture statement is presented as a real test or scan execution.
- [ ] Human decisions are recorded by the learner and no profile approves a release.

These runtime boxes remain unchecked in the supplied example because no live Copilot execution is claimed.
