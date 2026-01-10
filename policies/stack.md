# Stack
- Purpose: record the agreed technology stack for this repository. Fill this out before implementation.

## Languages and runtimes
- Languages: Go
- Runtimes/versions: Go 1.22.x (track latest patch in CI)

## Package manager
- Manager: Go modules
- Lockfile and constraints: go.sum tracked; run `go mod tidy` before commits to keep deps minimal

## Project types and targets
- Project types: Single-module Go template (library/CLI/service friendly)
- Build/test tooling: Go toolchain (gofmt, go vet, go test); optional staticcheck can be added later

## Deployment/CI notes
- CI provider: GitHub Actions (.github/workflows/ci.yml) running format check, go vet, and go test ./...
- Deployment targets (if any): none yet; future container/binary release to be decided

## Additional constraints
- Coding standards or policies to highlight: Follow policies/coding_standards.md, policies/testing_policy.md, and policies/commit_pr_rules.md
