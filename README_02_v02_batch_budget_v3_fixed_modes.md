# v02_batch_budget_v3_fixed_modes — Fixed mode iteration

## Files

- Original uploaded/generated filename: `patched_n8n_lead_workflow_batch_budget_v3_fixed_modes.json`
- Sanitized renamed filename: `workflows_sanitized/02_v02_batch_budget_v3_fixed_modes.sanitized.json`
- Original SHA-256: `cd9bd58cde36ee713959f8891d304957f7e5a1a3280dc48838025577ed49925a`
- Sanitized SHA-256: `176d6b717460639c6d50ac5fde38032aa90fdf121459d7910eaf55c232718be8`

## Verified structure

- Nodes: 59
- Connection keys: 52
- Node credential sections removed in sanitized copy: 17
- `.item` string references in original JSON: 15
- Budget found: No Search Strategy Config budget found in this file.

## Request/context that shaped this version

Iteration after mode-related fixing. Node set is the same as v01; changes are parameter/code-level.

## Change summary

No nodes added or removed from v01; used as a mode-fix iteration.

## Diff from previous version

- Previous node count: 59
- Current node count: 59
- Added nodes: 0
- Removed nodes: 0

## Known issue / caution

- Still not a full end-state workflow.
- Still before the later contact-first/manual-review/prospect-log fixes.

## Setup after import

1. Import the sanitized JSON into n8n.
2. Re-select credentials for CouchDB, Outscraper, Crawl4AI, DeepSeek, Google Sheets, and Discord.
3. Replace placeholders:
   - `<COUCHDB_PROXY_DOMAIN>`
   - `<CRM_DB_NAME>`
   - `<CRAWL4AI_HOST>` / `<CRAWL4AI_PORT>` or set `CRAWL4AI_BASE_URL`
   - `<GOOGLE_SHEET_SPREADSHEET_ID>`
   - `GOOGLE_SHEET_READY_GID`
   - `GOOGLE_SHEET_MANUAL_GID`
   - `<DISCORD_GUILD_ID>`
   - `<DISCORD_CHANNEL_ID>`
4. Run smoke test first.
5. Run live discovery with safe low budget before raising volume.

