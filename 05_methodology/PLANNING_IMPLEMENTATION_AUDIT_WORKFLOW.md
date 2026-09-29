# Planning → Implementation → Audit Workflow

## Roles

### ChatGPT / John

Architect, planner and independent auditor. Defines the phase contract, prepares the implementation prompt, checks evidence, scores the result and authorizes closure.

### Codex

Developer. Implements the approved scope, runs tests, updates the project, commits and pushes when the project uses GitHub, and reports exact evidence.

## Sequence

1. Plan one active phase here.
2. Freeze objectives, scope, acceptance criteria and exclusions.
3. Send Codex one precise implementation prompt.
4. Codex implements surgically and keeps the project runnable locally.
5. Codex runs relevant tests and reports branch, commit, changed files and preview.
6. ChatGPT audits independently for functionality, visual quality, regressions, security and reconciliation.
7. If needed, ChatGPT issues a correction prompt; Codex does not self-close the audit.
8. Close only when the evidence demonstrates the phase contract.

## GitHub and preview policy

- GitHub private by default.
- `main` is the stable DEMO reference.
- Work on `feature/*` from `develop` where applicable.
- Use Vercel Preview for web review and QA; do not publish production prematurely.
- Before pushing a completed implementation, run the project’s contract tests, lint and build.

## Evidence and packaging

- Keep a single canonical path and one active phase.
- ZIP only when it provides evidence needed for an independent audit or closure.
- Do not create ZIPs for micro-changes.
- The package must identify the base commit, new commit, changed files, commands, results, preview URL and known blockers.
- Internal “10/10” is only a candidate status. Final closure requires independent audit evidence.

## Status vocabulary

- `PLANNED`
- `IMPLEMENTATION_IN_PROGRESS`
- `IMPLEMENTATION_COMPLETE_PENDING_AUDIT`
- `READY_FOR_INDEPENDENT_AUDIT`
- `AUDIT_BLOCKED`
- `CORRECTION_REQUIRED`
- `CLOSED_10_10`
