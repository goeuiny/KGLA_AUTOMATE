# Repository instructions

## Required Codex operating policy

Before diagnosing, editing, testing, or reviewing, read and follow `CODEX_OPERATING_POLICY.md`.
It supplements this file; when instructions differ, follow the stricter safety, validation, and approval rule.

- Diagnose broadly in read-only mode before making a fix.
- Modify only the issue explicitly approved by the user; record unrelated findings without fixing them.
- Do not change live sends, production triggers, deployments, customer data, credentials, or live event output without explicit approval.
- If the same validation still fails after two targeted attempts, stop and report evidence, attempts, blockers, and safe next options.
- Do not claim completion without reproducible validation and a list of unverified areas.
- Use a separate read-only reviewer and isolated end-to-end validation for high-risk changes.

## Code Review Rules

- Review the selected diff against the original goal and the repository's non-negotiable behavior.
- Prioritize correctness, regressions, scope expansion, data loss, duplicate or missing operations, retries, time zones, security, external contracts, and missing tests.
- Reviewers report findings with severity, file evidence, trigger conditions, impact, and verification steps; they do not edit files.
- Treat tests and builds as evidence, not proof of external-service or production behavior.
- Return approved findings to the implementation chat, then run an independent review again after fixes.
