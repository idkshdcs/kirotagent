# Frontend Engineering

Load for implementation, code changes, responsive behavior, performance, SEO, or testing. Visual layout and breakpoint choices belong to `ui.md` to avoid duplicate rules.

## Project fit and code quality

- Inspect the real app entry points, routes, package manager, scripts, configuration, and affected components before changing them. Do not assume every project is a static `index.html`.
- Keep the current framework, architecture, naming, styling system, and dependency versions unless they block the request or the user asks for a change.
- Prefer focused patches, semantic HTML, scoped CSS, existing design tokens/components, and small, understandable functions. Avoid giant inline scripts, duplicate listeners, unnecessary globals, side effects during render, and direct DOM mutation where a framework owns the UI.
- Use real links for navigation and buttons for actions. Keep keyboard operation and focus behavior intact.
- Forms need clear labels, input validation, pending/disabled states where relevant, and useful success/error feedback. Validate security-sensitive input on the server.
- Avoid dependencies for small features that existing APIs or installed packages can handle safely. Keep manifests and lockfiles consistent; do not upgrade unrelated packages.

## Runtime behavior

- Every control must work as labelled, including navigation, buttons, forms, tabs, menus, dialogs, search, filters, sorting, import/export, and retry actions.
- Handle relevant loading, empty, validation, success, error, disabled, timeout, and retry states. Prevent duplicate submissions where appropriate.
- Render untrusted content safely. Do not use unsafe HTML injection for user-generated content unless a suitable sanitizer and explicit allowlist are in place.
- Handle network failures and malformed API responses without exposing private implementation details or stack traces.

## Performance and assets

- Avoid unnecessary packages, oversized bundles, duplicate requests, layout shifts, excessive rerenders, heavy animation loops, and unused font weights.
- Optimize images for their rendered size, reserve dimensions, lazy-load below-fold media, and do not lazy-load the primary hero by default.
- Measure before reporting performance scores. Never invent Lighthouse, Core Web Vitals, or bundle-size results.

## SEO and sharing

Apply only to public-facing pages where indexing/sharing matters:
- accurate title and concise description;
- correct document language and semantic headings;
- descriptive links and meaningful alt text;
- canonical URL only when the real canonical domain is known;
- Open Graph metadata when sharing matters;
- robots/sitemap rules appropriate to actual routes and deployment;
- structured data only for qualifying content and verified values.

Do not expose private routes, invent business facts, or promise indexing/rankings.

## Verification

1. Inspect available scripts/config before running commands; never invent commands.
2. When practical, run the cheapest safe baseline check relevant to the task and distinguish existing failures from regressions.
3. After editing, run the most relevant build, typecheck, lint, focused test, or browser check available. For a copy-only or tiny style change, a diff/syntax check may be enough.
4. For visible behavior, verify the changed user journey and only the responsive states relevant to the change, using the shared checkpoints in `ui.md`.
5. Never test destructively against production. If tools or scripts are unavailable, state what could not be checked.
