# Quality Gates
- Purpose: define concrete commands that must pass before merge. Align these with package scripts and CI.

## Lint
- Command: go vet ./...
- Notes: Run from module root; assumes go.mod is present.

## Format
- Command: gofmt -l .
- Notes: CI fails if any files are listed; developers may run `gofmt -w .` locally to auto-fix.

## Test
- Command: go test ./...
- Notes: Keep fast unit coverage; add `-count=1` or `-race` when code exists and performance allows.

## Failure handling
- Policy: Fix and rerun required before merge; any exception requires explicit human approval.
- Reporting: Record commands and outcomes in PRs per policies/commit_pr_rules.md; CI logs must show the same commands.
