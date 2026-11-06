# WebKirot 10.0

A focused skill for website and browser-facing web application work. The core file handles the everyday workflow; references are concise specialist notes loaded only when the task needs them.

## Files

- `skill-webkirot.md` — core web skill.
- `references/ui.md` — design direction, mockup intake, responsive and accessibility review.
- `references/frontend.md` — frontend engineering, performance, SEO, and verification.
- `references/product-integrity.md` — real CRUD, data-driven views, persistence, charts, and demo/live boundaries.
- `references/security.md` — authentication, authorization, secrets, sensitive actions, Discord/GetKey.
- `references/copy.md` — UI/product copy and localization.
- `references/advanced-mcp.md` — optional MCP and custom tooling, only when requested or clearly needed.

## Use

Keep `skill-webkirot.md` and its `references/` directory together. Reference paths are relative to the core file. Do not load every reference at session start; follow the trigger list in the core file.

If the host requires a conventional `SKILL.md` filename for importing a standalone skill, place this package in its own WebKirot skill folder and rename a copy of `skill-webkirot.md` to `SKILL.md` inside that folder. Do not overwrite a repository-level `SKILL.md` that serves as a general agent core.

## Design defaults

The user's preferences are defaults, not universal hard constraints. The current brand, supplied mockup, project design system, accessibility needs, and explicit request take priority.
