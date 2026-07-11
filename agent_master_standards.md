# Agent Master Standards

Repository-specific standards for this profile repository:

- Keep the visible profile surface in `README.md` as a single fixed-width terminal panel.
- When a visual reference is supplied, preserve its essential layout before selecting visual details.
- Render existing technology, tooling, and GitHub-stat information as CLI text; do not reintroduce badges, cards, graphs, or animations without requester direction.
- Describe agent capability through public workflow patterns only; never expose private project names, source, credentials, or business context.
- Treat `src/*.svg` and the `output` branch as legacy generated assets unless the README references them again.
- Do not commit provider error SVGs as successful profile assets.
- Use the self-hosted GitHub Readme Stats endpoint only as a validated source of textual metrics.
- Do not use broad staging commands in automation; stage only expected files.
- Do not use force-push or amend for routine profile refreshes.
- Do not record raw token, project ID, or secret values in repository files.
