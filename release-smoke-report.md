# Release Smoke Report — evidence pipeline dry run

- Account: HeziLiu
- Repository: mcpmark-eval-liuhezi/checklist-smoke (public, initialized with README.md, default branch `main`)
- Note on placement: repo creation was attempted under the personal account `HeziLiu` first and failed twice with a token-scope error (verbatim below). The repository was therefore created under the organization `mcpmark-eval-liuhezi` (an org the token can manage), which was the only path that permitted the must-have steps. The repository is public either way, so CI minutes do not touch private quota.
- Note on this file: the report was intended for a **secret gist** named `release-smoke-report.md`, but gist creation is blocked by the same token-scope error (verbatim below, attempted twice). This file is the substitute evidence artifact, kept in this repo so the proof is in one forwardable place.

Verbatim personal-account repo creation error (attempted twice):
```
failed to create repository: POST https://api.github.com/user/repos: 403 Resource not accessible by personal access token []
```

Verbatim gist creation error (attempted twice):
```
failed to create gist: POST https://api.github.com/gists: 403 Resource not accessible by personal access token []
```

## Pull request

- Number: 1
- Title: Add Release Checklist to README
- State: open (not merged, not draft)
- Base: `main` ← Head: `checklist-update`
- Commits: 1
- Changed files:

| file | status | additions | deletions |
| --- | --- | --- | --- |
| README.md | modified | 9 | 0 |

## Workflow run

Checked at the moment of report generation (run id 39673077256, run_number 1, event `workflow_dispatch`, head branch `main`, head sha 5d419432428b9ba7d12e804f0468c6b0fa0a5ad3):

- Run status: `completed` (conclusion: `success`)

Jobs:

| job | status | conclusion |
| --- | --- | --- |
| smoke | completed | success |

(Exactly one run of `.github/workflows/smoke.yml` was triggered; the workflow is on-demand only via `workflow_dispatch` and contains a single trivial job whose one step echoes the marker `SMOKE_PIPELINE_CHECK_OK`.)

## Inbox

The notifications check failed with a token-scope error and returned no data (attempted twice). Verbatim error:

```
failed to list notifications: GET https://api.github.com/notifications?page=1&per_page=30: 403 Resource not accessible by personal access token []
```

## Teams

The team-membership check succeeded but returned no team memberships: the call for user HeziLiu returned a single organization entry `mcpmark-eval-liuhezi` with an empty team list (`{"org":"mcpmark-eval-liuhezi","teams":[]}`). So: no team memberships returned.

## Computed stats

Computed in Python 3.13.12 with pandas 2.3.1 (pandas verified installed before the stats step; no install needed).

- Number of changed files: 1
- Total additions: 9
- Total deletions: 0

FINGERPRINT=b335630551682c19a781afebcf4d07bf978fb1f8ac04c6bf87428ed5106870f5

(Fingerprint = SHA-256 of the changed file paths sorted alphabetically and joined with newline characters, UTF-8 encoded, no trailing newline.)
