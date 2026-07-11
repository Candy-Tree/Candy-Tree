# Component Data Flows

## README.md

- Input: profile-avatar ASCII text, current technology/tool information, a public agent-capability summary, and stable text fields for scheduled GitHub metrics.
- Process: GitHub renders one Markdown code block into a neofetch-style profile page.
- Output: avatar ASCII on the left and aligned stack/tool/GitHub-stat/agent-capability fields on the right.
- Dependencies: GitHub README renderer.

## .github/workflows/main.yml

- Input: scheduled/manual/push workflow events and `secrets.GITHUB_TOKEN`.
- Process: download and validate the self-hosted stats SVG, parse its textual counters, fetch public GitHub counters, replace README terminal fields, and commit only the README if changed.
- Output: refreshed `README.md` terminal metrics.
- Dependencies: GitHub Actions, self-hosted stats provider, GitHub public API, GitHub repository write permission.

## src/*.svg

- Input: legacy SVG responses downloaded by the prior workflow.
- Process: retained in the repository but not consumed by the current README or workflow.
- Output: no visible profile surface.
- Dependencies: none in the current design.

## output branch

- Input: legacy snake animation assets.
- Process: retained without active writes.
- Output: no visible profile surface.
- Dependencies: none in the current design.
