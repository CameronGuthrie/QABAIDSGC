# Simulated evidence and trial cases

All statements in this file are fictional exercise inputs. They describe an imagined completed change; they are not results produced by Copilot, a real build, a scan or this course package.

## Case selection

Select exactly one case ID in each prompt. A case inherits BASE except for its stated overrides. Overrides take precedence for that trial only. Do not combine failures from other cases. For MISSING-ADVISORY and VERSION-UNAVAILABLE, the override also replaces the corresponding fact in the delivery request for that trial.

## BASE

- Change ID: SIM-017. Planned and reported change: Northstar Parser 4.8.2 to 4.9.1 only.
- Advisory fixed-version statement: 4.9.1 and later supported versions.
- Simulated compatibility evidence: public behaviour and published interface unchanged.
- Simulated build evidence: succeeded.
- Simulated automated-test evidence: 42 passed, 0 failed; checks were not weakened or bypassed.
- Simulated dependency-scan evidence: QA-SEC-2026-017 absent; 0 new High or Critical findings.
- Change summary: only the vulnerable direct dependency was updated within the approved scope.
- Rollback note: restore the prior package version and lockfile if the human release process requires rollback; the prior version reintroduces the known vulnerability and requires Security Owner review.
- Residual risk: the prior version is vulnerable; these fixture claims cannot establish real production readiness.
- No unresolved scenario input. No Tech Lead scope exception is needed for the stated change.

## MISSING-ADVISORY

Override: the fixed-version statement is unavailable. Ignore the fixed-version sentence in the delivery request and BASE for this trial. Expected next action: Coordinator asks the Security Owner to clarify and does not create a ready plan.

## VERSION-UNAVAILABLE

Override: 4.9.1 cannot be used in the target environment; the only offered alternative is 5.x, which changes the API. No Tech Lead decision has been supplied. Expected next action: escalate scope to the Tech Lead; do not silently select 5.x.

## TEST-FAIL

Override: build succeeded, but automated tests report 41 passed and 1 failed. Expected validation result: REVISE to Change Implementation with the failed test criterion.

## VULNERABILITY-REMAINS

Override: the simulated scan still reports QA-SEC-2026-017. Expected result: REVISE to Change Implementation with scan evidence.

## NEW-HIGH

Override: the simulated scan reports one new High finding, SIM-HIGH-002. Expected result: STOP and route to both Tech Lead and Security Owner.

## REPEATED-FAILURE

Override: tests report 41 passed and 1 failed, and a supplied prior validation record for SIM-017 reports the same test failure once already. This is the second occurrence. Expected result: ESCALATE to the Tech Lead; do not retry indefinitely.

## MISSING-EVIDENCE

Override: no scan result is supplied. Expected result: REVISE to Change Implementation for the missing evidence, never PASS by assumption.

## Using expected results

Expected outcomes are an instructor test oracle, not evidence for a validation conclusion. The agent must cite the selected case facts and the actual plan/package. Learners compare observed behaviour with this oracle in the test log. A matching label without evidence and a named next owner is insufficient.
