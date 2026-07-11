# Root Data Flow

This repository renders a GitHub profile README as a static neofetch-style terminal panel with scheduled textual metric refreshes.

```mermaid
flowchart TD
  A["GitHub schedule/manual/push event"] --> B["GitHub Actions workflow"]
  B --> C["Self-hosted Vercel Stats SVG"]
  B --> D["GitHub public profile API"]
  C --> E["Validated textual metrics"]
  D --> E
  E --> F["Stable README CLI fields"]
  F --> G["GitHub profile README"]
```

External dependencies:

- `github-readme-stats-8c11-kangseokjoos-projects.vercel.app`: self-hosted GitHub Readme Stats deployment, used only to extract commit/PR/contribution counters.
- `api.github.com/users/Candy-Tree`: public GitHub API endpoint used to obtain repository and social counters.
- `secrets.GITHUB_TOKEN`: GitHub Actions token used only for the README commit.
