# Changelog

## 10.0.0 — 2026-11-06

Major restructuring based on review of V9.0, V8.2 references, and observed issues in the Discord GetKey, NexusWork V1, and Taskify V2 website experiments.

- Rewrote the core as a short operational workflow with Tiny / Normal / High-impact paths.
- Removed mandatory receipt, mandatory Task Ledger, chessboard metaphor, simulated three-role review, and default MCP orchestration.
- Made MCP an optional specialist reference; direct tools and existing project commands remain the default.
- Added an explicit screenshot/mockup intake process without requiring unnecessary confirmation for reversible visual choices.
- Split visual design (`ui.md`) from engineering (`frontend.md`), with shared responsive breakpoints owned only by `ui.md`.
- Added a dedicated copy reference for UI wording, error/empty states, localization, and truthful marketing copy.
- Retained and refined `product-integrity.md` because prior dashboard/GetKey evaluations exposed real gaps in CRUD, search/filter/sort, chart provenance, persistence, and fake-live behavior.
- Consolidated security and Discord/GetKey server boundaries in `security.md`.
- Preserved personal design preferences as overridable defaults, not mandatory rules or animation quotas.
- Added proportional verification, clear evidence labels, and a stop condition to prevent review loops.

### Migration notes

- V9.0 `ui-quality.md` is now split into `ui.md` and `frontend.md` to separate design decisions from implementation engineering.
- V9.0 `security-permissions.md` becomes `security.md`.
- V9.0 `mcp-advanced.md` is refined as `advanced-mcp.md` and remains opt-in.
- V9.0 `product-integrity.md` is retained as a dedicated module.
- `copy.md` is new.
- This is a restructure, not a claim of external browser/runtime testing. The package structure and relative references are validated locally.
