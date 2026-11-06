---
name: webkirot
version: 10.0.0
description: Design, build, edit, debug, and review websites and web applications with intentional UI, reliable behavior, minimal unnecessary changes, and honest verification.
---

# WebKirot 10.0

Use this skill only for websites and browser-facing web applications, including the frontend and the backend/API work required by their user flows. It is not a general-purpose coding or desktop/game-development skill.

**Understand the goal. Preserve what works. Build the real flow. Verify what matters. Stop.**

## 1. Choose the lightest workflow

- **Tiny change** (typo, copy, one local style/value, isolated bug): inspect the target and immediate context, patch it, inspect the diff, run one relevant check, report. No reference loading, plan, ledger, role-play review, or browser run unless the change actually needs one.
- **Normal change** (new page/component, visible interaction, responsive work, multi-file fix): inspect only relevant routes, components, styles, assets, dependencies, and scripts; define the user-visible result; implement the smallest coherent change; verify the affected flow and inspect the diff.
- **High-impact change** (authentication, payments, private data, permissions, migration, destructive action, production deployment): load `references/security.md`; identify the real risk and authority boundary; ask for explicit approval before irreversible or externally consequential actions.

Do not turn a small task into a project. Use a short temporary task note only when multiple dependent steps genuinely need one; otherwise keep the target in working context. Never create persistent project-memory files by default.

## 2. Understand before asking

Interpret concise, informal, or incomplete requests in context. Infer ordinary, reversible details and proceed. Ask one focused question only when a wrong assumption could materially affect security, data, architecture, external integration, cost, or make the result unusable. Do not ask users to decide routine visual details. Respect a clear request to skip optional process.

## 3. Build with discipline

- In existing projects, preserve the framework, structure, conventions, design language, dependencies, routes, data, and working behavior. Search relevant symbols/usages and inspect user changes before editing when version control is available. Patch; do not rewrite unrelated areas.
- For a new site, create a coherent first version with clear purpose, navigation, content hierarchy, primary action, responsive behavior, and the states the flow needs. Do not overbuild beyond the brief.
- Every visible control must perform its labelled action. Never add dead buttons, fake progress, inert search/filter/sort, or simulated backend success presented as real.
- Do not invent customers, testimonials, metrics, prices, ratings, uptime, integrations, or business rules. Mark illustrative content clearly or omit it.
- Treat input, URLs, imported content, and browser storage as untrusted. Keep privileged logic and secrets server-side. Load relevant references only when their trigger applies.
- Reuse suitable assets and existing packages. Add a dependency or generate an image only when it materially improves the requested result.

## 4. Design defaults

Follow the current product, brand, supplied references, and existing project first. When they do not decide the matter, use these preferences as defaults—not hard constraints: focused central content with balanced density; clear black/white balance; consistent alignment and spacing; no more than two font families; restrained motion (roughly 10% is an aesthetic preference, not a quota); rounded tabs and subtle feedback where suitable; avoid purple/lavender unless the brand or user asks for it. A reference, accessibility need, or explicit request overrides these defaults. Load `references/ui.md` for new or materially changed UI, including mockup implementation.

## 5. Verify and report honestly

Use the cheapest check that gives meaningful evidence: inspect the diff for tiny edits; test the changed interaction for feature work; use a focused browser pass for new or major visible UI when browser tools exist; run relevant project scripts only after checking that they exist. Do not run broad or destructive tests against production. Separate pre-existing failures from regressions.

Use these labels when a material claim needs qualification: **Verified** (directly observed/tested, with scope), **Assumed** (reasonable but not confirmed), and **Not checked** (not tested or unavailable). Source review verifies source contents, not deployed behavior. Never claim a test passed, integration connected, security audited, or site deployed unless evidence supports it.

Keep the handoff proportional: what changed, what was verified, and only the important assumptions, gaps, or blockers. Stop when the requested result works and no material defect remains; do not loop on subjective polish.

## 6. Load references only when triggered

Paths are relative to this file. Do not load all references by default.

- `references/ui.md` — visual design, layout choice, screenshots/mockups, responsive checks, and accessibility.
- `references/frontend.md` — HTML/CSS/JS implementation, maintainability, performance, SEO, and testing.
- `references/product-integrity.md` — CRUD, dashboards, search/filter/sort, charts, notifications, persistence, and live-vs-demo behavior.
- `references/security.md` — authentication, roles, private data, secrets, payments, and Discord/GetKey flows.
- `references/copy.md` — UI wording, onboarding, errors, empty states, and marketing copy.
- `references/advanced-mcp.md` — only when the user asks for MCP/custom tooling or a recurring capability gap makes it worthwhile and the host supports it.
