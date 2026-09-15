# Acceptance Criteria, Constraints and Authorities

## Acceptance criteria

A remediation result is considered ready for human release review only when all of the following are true:

1. The vulnerable direct dependency is upgraded to a version covered by the advisory's fixed-version statement.
2. The chosen change does not intentionally alter the service's public behaviour or published interface.
3. The existing build and automated test suite complete successfully.
4. A dependency/security scan no longer reports **QA-SEC-2026-017** for the service.
5. No new High or Critical dependency finding is introduced by the remediation.
6. The change package contains a concise change summary, validation evidence, known residual risks, and a rollback note.
7. Any unresolved uncertainty is visible rather than being filled with an unsupported assumption.

## Constraints

- Prefer the smallest safe remediation that satisfies the approved request.
- Do not change unrelated dependencies.
- Do not disable, weaken or bypass tests, quality gates or security scanning.
- Do not suppress the advisory as a way of making the finding disappear.
- Do not make a breaking major-version upgrade without an explicit human decision.
- Do not deploy to production from an AI-agent workflow.
- Agents may prepare evidence and recommendations, but a person owns the consequential release decision.

## Human authorities

### Security Owner
Owns the interpretation of the advisory when its meaning, affected versions or required security outcome is unclear.

### Tech Lead
Owns decisions that materially change implementation scope, including a breaking version change, a wider refactor, or an exception to the original delivery constraints.

### Release Owner
Owns the final release decision. The permitted outcomes are **Approve**, **Revise**, **Escalate** or **Stop**.

## Exception conditions that must be handled

- Required advisory information is missing or contradictory.
- Version 4.9.1 cannot be used in the target environment.
- The smallest safe upgrade causes test or compatibility failures.
- Validation finds that the security issue is still present.
- Validation reveals a new High or Critical dependency finding.
- The same remediation attempt fails validation repeatedly.
