# Release Smoke Test Report

Evidence report for the end-to-end checklist-smoke dry run. All live data reported as-is.

## Pull request

- Number: #1
- Title: Add Release Checklist to README
- Changed files (as reported by GitHub):
  - README.md: additions 9, deletions 0, status modified
- Total changed files: 1
- Total additions: 9
- Total deletions: 0

## Workflow run

- Workflow: Smoke Check (.github/workflows/smoke.yml), run #3, id 41258314002
- Branch: main, event: workflow_dispatch
- Run status at time of check: in_progress
- Jobs:
  - smoke: status completed, conclusion success
    - Steps: Set up job (completed/success), Echo smoke marker (completed/success), Complete job (completed/success)

## Inbox

- My current notifications could not be retrieved. The notifications API returned a 403 error:
  "failed to list notifications: GET https://api.github.com/notifications?page=1&per_page=50: 403 Resource not accessible by personal access token []"
- A second attempt with the participating filter returned the same 403:
  "failed to list notifications: GET https://api.github.com/notifications?page=1&participating=true&per_page=50: 403 Resource not accessible by personal access token []"
- Note: no notifications were returned due to the token lacking the notifications scope.

## Teams

- get_teams for HeziLiu returned one organization: mcpmark-eval-liuhezi, with teams: [] (empty).
- Note: no team memberships were returned for the authenticated user.

## Computed stats

- Number of changed files: 1
- Total additions: 9
- Total deletions: 0
- FINGERPRINT=b335630551682c19a781afebcf4d07bf978fb1f8ac04c6bf87428ed5106870f5

## Errors encountered during the run

- Personal-account repository creation failed with:
  "failed to create repository: POST https://api.github.com/user/repos: 403 Resource not accessible by personal access token []"
- Notifications listing failed with:
  "failed to list notifications: GET https://api.github.com/notifications?page=1&per_page=50: 403 Resource not accessible by personal access token []"
- Gist creation failed with:
  "failed to create gist: POST https://api.github.com/gists: 403 Resource not accessible by personal access token []"
- Workaround applied: the scratch repository checklist-smoke already existed under the organization mcpmark-eval-liuhezi (public, README.md initialized, .github/workflows/smoke.yml present with a workflow_dispatch trigger and a single smoke job echoing SMOKE_PIPELINE_CHECK_OK). The repo name starts with checklist-smoke as required. This report is Mirrored as release-smoke-report.md in the repo root as fallback evidence.
