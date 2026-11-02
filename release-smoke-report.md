# Release Smoke Report — Evidence Pipeline Dry Run

Account: HeziLiu (https://github.com/HeziLiu)
Repository: mcpmark-eval-liuhezi/checklist-smoke (public, initialized with README.md, default branch `main`)
Workflow: .github/workflows/smoke.yml on `main` — on-demand `workflow_dispatch`, single job `smoke`, one step echoing `SMOKE_PIPELINE_CHECK_OK`
Branch: checklist-update README.md gained a `## Release Checklist` section (read back and confirmed present)
PR: #1 "Add Release Checklist to README", open, base `main` <- head `checklist-update`

## Pull request

- Number: 1
- Title: Add Release Checklist to README
- State: open (not merged, not draft)
- Base: `main` <- Head: `checklist-update` (sha b98fcf5ea3837683eb791450f87d06da7ac67d30)
- Commits: 1
- Changed files:

| file | status | additions | deletions |
| --- | --- | --- | --- |
| README.md | modified | 9 | 0 |

- Totals: number of changed files = 1, total additions = 9, total deletions = 0

## Workflow run

Checked at the moment of report generation (run id 41258314002, run_number 3, event `workflow_dispatch`, head branch `main`, head sha 550c377fe2c5eba9a2a385da66d14682bbca15ee):

- Run status: `completed` (conclusion: `success`)

Jobs:

| job | status | conclusion |
| --- | --- | --- |
| smoke | completed | success |

(Exactly one run of `.github/workflows/smoke.yml` was triggered; the workflow is on-demand only via `workflow_dispatch` and contains a single trivial job whose one step echoes the marker `SMKE_PIPELINE_CHECK_OK`.)

## Inbox

The notifications check failed with a token-scope error and returned no data (attempted with filters `default` and `only_participating`). Verbatim errors:

```
failed to list notifications: GET https://api.github.com/notifications?page=1&per_page=50: 403 Resource not accessible by personal access token []
```

```
failed to list notifications: GET https://api.github.com/notifications?page=1&participating=true&per_page=50: 403 Resource not accessible by personal access token []
```

No notifications were returned (the inbox check could not be satisfied due to the personal access token lacking the notifications scope).

## Teams

The team-membership check succeeded but returned no team memberships: the call for user HeziLiu returned a single organization entry `mcpmark-eval-liuhezi` with an empty team list (`{"org":"mcpmark-eval-liuhezi","teams":[]}`). So: no team memberships returned.

## Computed stats

Computed in Python 3.13.12 with pandas 2.3.1 (verified installed before the stats step; no install needed).

- Number of changed files: 1
- Total additions: 9
- Total deletions: 0

FINGERPRINT=b335630551682c19a781afebcf4d07bf978fb1f8ac04c6bf87428ed5106870f5

(Fingerprint = SHA-256 hex digest of the changed file paths sorted alphabetically and joined with newline characters, UTF-8 encoded, no trailing newline.)

## Gist attempt (failed)

Attempted to create a secret gist with filename `release-smoke-report.md`. The call failed with a token-scope error; verbatim error:

```
failed to create gist: POST https://api.github.com/gists: 403 Resource not accessible by personal access token []
```

The report above is therefore stored in the repository file `release-smoke-report.md` on branch `main` (https://github.com/mcpmark-eval-liuhezi/checklist-smoke/blob/main/release-smoke-report.md) as the forwardable evidence artifact.
