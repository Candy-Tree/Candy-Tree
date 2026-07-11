# Architecture Analysis

This is a small GitHub profile repository. It has no application runtime, package manager, build system, or production source modules.

Primary ownership boundaries:

- `README.md` owns the visible neofetch-style terminal composition.
- `.github/workflows/main.yml` owns scheduled refresh of textual GitHub metrics in the README.
- `src/*.svg` stores legacy generated visual assets that are not displayed by the current README.
- The `output` branch stores legacy snake animation output that is not displayed by the current README.

Data shape:

- The README contains one ASCII-only Markdown code block and no visible external images.
- The workflow fetches a Vercel Stats SVG only to parse validated numeric values from its SVG description.
- The workflow combines those values with public GitHub API counters, then replaces stable CLI field labels inside the README.
- The agent trend and capability fields are static public-profile text; the workflow does not mutate them.

Risk notes:

- A provider can return an error SVG with HTTP 200. The workflow must inspect content, not only file size.
- The README metric field labels are a contract with the workflow. Renaming them requires updating the replacement script.
- The local checkout can lag behind remote workflow-generated updates. Avoid broad staging such as `git add *`.
