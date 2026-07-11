# Walkthrough

## 2026-07-03

- Inspected repository layout: `README.md`, `.github/workflows/main.yml`, and `src/*.svg`.
- Found local error SVGs for stats, top languages, streak, and contribution graph.
- Confirmed live stats provider response returned a valid stats card with `Total Commits: 149`.
- Confirmed remote GitHub Actions workflow runs were succeeding on schedule through public GitHub API data.
- Confirmed `VERCEL_PROJECT_ID` is set locally and `VERCEL_TOKEN` is not set.
- Updated README URLs with `cache_seconds=21600` and `v=` cache keys.
- Reworked the workflow to run daily, generate snake first, validate downloaded SVG contents, refresh README cache keys, commit only expected files, and avoid force-push.
- Refreshed local `src/statCard.svg`, `src/mostUsed.svg`, and `src/contributionGraph.svg` from verified live responses.
- Left `src/streak.svg` unchanged because additional network verification was blocked; the README now uses the live streak URL and the workflow treats streak cache refresh as optional.
- Validated workflow YAML parsing and README cache-key replacement locally.

## 2026-07-10

- Researched ASCII art as a text-native visual technique using printable characters.
- Read the current profile README and preserved its existing technology/tool information: Android, Kotlin, Swift, Firebase, Bitrise, Google Play, GitHub, Notion, Slack, Asana, Postman, and Insomnia.
- Replaced the local README composition with a Candy-Tree terminal banner, a terminal-formatted profile summary, and existing stats/activity/snake assets.
- Built the design in an isolated Markdown preview first. Validation confirmed balanced code fences, a maximum ASCII-art width of 57 columns, and ASCII-only banner content.
- Did not commit, push, deploy, or otherwise reflect the change remotely.
- The requester rejected the initial result because it did not match the neofetch-style visual reference and because it retained visible cards rather than transforming their information into CLI text.
- Downloaded the public Candy-Tree avatar to a temporary location, converted it to high-density ASCII in a scratch harness, and used the smoothed result as the left side of the terminal panel.
- Replaced the README with one neofetch-style code block. The right side contains existing Android/Kotlin/Swift, service, tool, and API-client information plus verified public GitHub counters.
- Replaced card/snake asset generation with a daily workflow that validates the Vercel Stats SVG, fetches public GitHub API counters, and updates only the README terminal fields.
- Validated the final README as a single balanced ASCII block with no image, badge, graph, or snake references. Executed the actual workflow refresh step in a temporary harness with fixture responses; all six metric fields updated successfully.
- Did not commit, push, deploy, or otherwise reflect the corrected design remotely.
- The requester supplied a replacement photo because the previous public-avatar ASCII was difficult to recognize. Cropped the photo around the face, converted it with inverse luminance mapping so its bright subject is rendered as visible text, and replaced only the left-side ASCII portrait.
- Preserved all right-side CLI fields and the workflow's six stable metric labels. Did not commit, push, deploy, or otherwise reflect the photo replacement remotely.
- Final validation measured a 112-column terminal panel after the higher-resolution photo conversion.
- Researched current agent-development practice from primary sources and added four static fields below the README refresh field: tool use/orchestration/tracing/evals, plan-delegate-verify-deliver workflow, multi-agent developer-workflow scope, and private-context handling.
- The agent summary excludes private project identities, source code, credentials, and business context.
- Validated the 128-column terminal panel and ran the workflow-equivalent Perl replacement logic in an isolated harness. All six metric fields updated while the new agent fields remained intact.
