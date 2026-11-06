# UI Design, Visual Direction, and Mockups

Load for a new website, a meaningful visual change, responsive work, or implementation from a supplied screenshot/wireframe. This file owns the visual review and shared responsive checkpoints; `frontend.md` should not duplicate them.

## Choose by purpose

Choose the simplest layout that makes the visitor's main task obvious:
- **Landing/product:** top navigation, focused introduction, proof/content, clear primary action.
- **SaaS/workspace:** sidebar or top navigation plus a persistent work area; use tabs only for closely related views.
- **Data/admin:** compact table/list with search, filters, sorting, and row actions when scanning records matters; use cards only when comparison or summary benefits.
- **Settings:** grouped sections or local tabs for related configuration.
- **Wizard/get-key flow:** clear ordered steps only when the process truly has sequential stages.
- **Editorial/docs:** readable column, strong heading hierarchy, useful in-page navigation when long.
- **Product/service/place:** show the real product, work, people, or place; organize details around the visitor's decision or next action.
- **Bento/cards:** use for a small set of related summaries or independent entry points, not as a default page template.

Do not present a layout menu unless the user is exploring options. For a direct build request, choose and proceed. Avoid stacking patterns just to make the page look complex.

## Visual system

- Follow supplied brand/reference and existing project decisions. Otherwise establish one coherent set of semantic color roles, spacing, typography, borders, radii, surfaces, and states.
- Prioritize hierarchy, alignment, readable content width, and useful information density. Whitespace should organize content, not leave the central work area unnecessarily empty.
- Avoid generic gradients/glass, repetitive cards, oversized empty heroes, decorative clutter, or arbitrary effects unless they fit the product.
- Use motion for feedback, state, or useful transitions; respect `prefers-reduced-motion`. Never treat the user's approximate motion preference as a numeric requirement.
- Use real project/product imagery when available. Prefer CSS/SVG for simple shapes, icons, and diagrams. Do not fabricate logos, customers, screenshots, testimonials, certifications, or real-world business photos.

## Screenshot / mockup intake

1. Inspect the supplied image before coding. Identify the viewport and observable regions, hierarchy, alignment, proportions, spacing, typography character, color roles, borders/shadows, image crop, and visible states.
2. Separate **observed** details from **estimated** values. Do not claim guessed font names, hex colors, or pixel measurements are exact.
3. Build a compact target map of major regions and relationships; do not write a long visual essay unless asked.
4. Reuse the project's stack and components. Recreate the visual intent responsively rather than shrinking a desktop screenshot literally. Infer unseen behavior conservatively.
5. If a consequential detail is ambiguous (for example, a missing mobile navigation model or an unknown action), ask one focused question. Otherwise choose a reversible default and proceed; do not require approval for every visual inference.
6. When browser/screenshot tools are available, compare one rendered pass with the reference. Fix the largest gaps first: structure/proportions, hierarchy, typography, color, then fine details.

## Responsive and accessibility review

Use these shared checkpoints when relevant: **320 / 390 / 768 / 1024 / 1440 px**. They are not a requirement to render every width for every task. For a tiny edit, check only the affected area; for a new or major layout, check representative narrow, medium, and wide states.

Check for horizontal overflow, clipping, overlap, unusable navigation, readable type, touch-friendly controls, semantic elements, accessible names, associated form labels, keyboard operation, visible focus, logical focus order, meaningful alt text, and states not conveyed by color alone. Aim for WCAG AA contrast where practical. Support reduced motion. One visible `h1` is a useful page-level default where meaningful, not a forced rule for every SPA view or component.

## One-pass visual review

Review the changed path once from the visitor's perspective: purpose/action, hierarchy, consistency, actual control behavior, responsive layout, focus/keyboard use, and relevant empty/loading/error states. Fix material issues in one focused pass. Do not run the same checklist again under another reference or chase subjective perfection.
