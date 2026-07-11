# Implementation Plan

## Status

The neofetch-style redesign is implemented locally with a requester-supplied-photo ASCII portrait and awaits requester review. It has not been committed, pushed, or deployed.

## Plan

1. Re-read the README and profile context after requester feedback, and inspect the visual reference. Completed.
2. Convert the public Candy-Tree avatar into a high-density ASCII preview in an isolated scratch area. Completed.
3. Build one neofetch-style terminal panel: avatar ASCII on the left and only verified stack/tool/GitHub information on the right. Completed.
4. Remove visual badges, stats cards, graph, and snake output from the README. Preserve their information as CLI fields instead. Completed.
5. Update the refresh workflow so the README's textual GitHub-stat fields can be refreshed without reintroducing cards. Completed.
6. Validate the final Markdown, ASCII dimensions, and workflow syntax, then show the local uncommitted result. Completed.
7. Replace the original public-avatar ASCII with an ASCII conversion of the requester-supplied photo while preserving the terminal layout and metric field labels. Completed.
8. Add a public agent-trend and capability summary below the refresh field without exposing private-project details. Completed.

## Constraints

- The requester explicitly asked for no remote reflection; the README must remain local and uncommitted.
- Existing Vercel Stats data is retained only as a data source for textual metrics, not as a visible SVG card.
- The README must not display visual badges, stats cards, contribution graphs, or snake animation in this redesign.
