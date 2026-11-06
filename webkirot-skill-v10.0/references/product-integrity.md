# Product Integrity and Data-Driven UI

Load for dashboards, CRUD, admin panels, search/filter/sort, Kanban, charts, notifications, persistence, API integrations, or any page presenting live status or metrics.

## Identify what is real

Use explicit labels when users could mistake a demo for a connected product:
- **LIVE / REAL:** connected to the actual service/data source and verified.
- **DEMO / SAMPLE:** illustrative data or a local-only flow.
- **PLACEHOLDER:** awaiting real values or integration.
- **UNAVAILABLE:** service/capability is not connected or currently usable.
- **ESTIMATE:** calculated approximation with its basis explained.

A frontend-only prototype may demonstrate a flow, but must label it honestly. Never claim a key was verified, payment completed, bot came online, message was sent, or data saved remotely unless the real operation succeeded.

## Check controls by behavior

For each important control, identify its input, action, state change, and feedback:
- **CRUD:** validate inputs; implement real create/read/update/delete; update every dependent view; handle empty, duplicate, and error cases where relevant.
- **Search:** define its scope and fields; verify results change as the query changes and empty results are clear.
- **Filter:** verify each filter changes the displayed set and combines correctly with other active filters.
- **Sort:** verify the selected field and direction actually reorder the records. Do not show a decorative sort control.
- **Kanban/status:** persist changes, move records to the correct column, and update related counts/progress.
- **Relationships:** define what happens to child records when a parent is deleted or changed; do not leave orphaned or misleading data.
- **Charts/analytics:** derive values from the same current dataset as the product. Clearly mark sample series; never present hardcoded demo history as live analytics.
- **Notifications/activity:** distinguish real events from static examples; counts and unread state must match the list.
- **Settings/theme:** if persistence is promised, verify the value saves and restores after reload.
- **Import/export/reset:** validate schema and format; explain destructive reset; do not silently overwrite recoverable data.

## Data consistency and resilience

Keep cards, tables, filters, charts, detail views, and totals consistent after mutations. Validate loaded/imported data shapes and types. Handle malformed JSON, missing fields, older schema versions, quota/storage errors, and unavailable storage where relevant. Do not silently discard user data after a parse or migration failure; preserve a recoverable copy or explain the issue before reset.

Use coherent sample dates and totals for the stated scenario. Clearly label fixtures. Distinguish derived metrics from manually entered values and explain the formula/source when it affects interpretation.

## Completion check

Test the core user journey and the most relevant empty/failure state. After mutations, verify exposed dependent counts, charts, filters, and persisted state. Inspect the focused diff and stop when acceptance checks pass; do not audit unrelated features.
