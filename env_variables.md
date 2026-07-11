# Environment Variables

Sensitive values must not be printed or committed.

| Name | Scope | Purpose | Value Handling |
| --- | --- | --- | --- |
| `VERCEL_PROJECT_ID` | Local/Codex environment | Identifies the Vercel project `candytree-labs/github-readme-stats-8c11` when a Vercel API or CLI token is available. | Present locally; value intentionally not recorded. |
| `VERCEL_TOKEN` | Local/Codex environment | Would be required to inspect Vercel project settings through the Vercel API. | Not present locally during this task. |
| `GITHUB_TOKEN` | GitHub Actions secret context | Allows the workflow to commit README/SVG updates and publish the `output` branch. | Provided by GitHub Actions as `secrets.GITHUB_TOKEN`; no raw value is stored. |
| `CACHE_SECONDS` | GitHub Actions workflow env | Sets the GitHub Readme Stats cache query value. | Non-secret constant: `21600`. |
| `PROFILE_USER` | GitHub Actions workflow env | GitHub login rendered by stats providers. | Non-secret constant: `Candy-Tree`. |
