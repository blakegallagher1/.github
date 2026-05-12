# .github

Shared reusable workflows and community health files for [blakegallagher1](https://github.com/blakegallagher1) repos.

## Reusable workflows

| File | Purpose |
|------|---------|
| [`.github/workflows/reusable-ci.yml`](.github/workflows/reusable-ci.yml) | Opinionated Node install + lint/typecheck/test/build (defaults to npm scripts). |
| [`.github/workflows/reusable-smoke-health.yml`](.github/workflows/reusable-smoke-health.yml) | Minimal `workflow_call` ping to verify `uses:` wiring from downstream repos. |

### Pinning callers

- Prefer **`uses: blakegallagher1/.github/.github/workflows/<file>.yml@<full_sha>`** so `main` refactors cannot change behavior under you.
- Optional **semver tag**: `...@reusable-smoke-v1` (see Git tags); repoint the tag only when callers are ready.

### Org-level defaults

Default community templates only aggregate for **organizations** in GitHub docs. User-owned repos should keep explicit `uses:` or copy templates locally.
