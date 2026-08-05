# v00_initial — Initial imported workflow baseline

## Files

- Original uploaded/generated filename: `lead_discovery_workflow_v2.json`
- Sanitized renamed filename: `workflows_sanitized/00_v00_initial.sanitized.json`
- Original SHA-256: `878887252afa3c5ed441abb683f64e2dbfcf08cfc9a13a3c214205804ae517cd`
- Sanitized SHA-256: `360ee861a1c43cad03cafd2b8fd96c8154800d59aa122a161372d7fd82c69e9a`

## Verified structure

- Nodes: 90
- Connection keys: 75
- Node credential sections removed in sanitized copy: 31
- `.item` string references in original JSON: 24
- Budget found: queries_per_run: 10, outscraper_limit_per_query: 20, raw_domain_pool_per_run: 120, new_companies_to_crawl_per_run: 15, max_deep_pages_per_company: 2, max_deepseek_prequal_per_run: 35

## Request/context that shaped this version

Original baseline file supplied as the starting point. Treat this as the source lineage, not the recommended final build.

## Change summary

No previous version in this package.

## Known issue / caution

- High paid Maps exposure in baseline budget: 10 queries × 20 places when Search Strategy Config is present.
- Several nodes still had `.item` paired-item usage risk after HTTP/bulk/branch nodes.
- Google Sheet append was per item and used batchUpdate in a way that later showed row overwrite/race behavior.
- Credentials and live service identifiers existed in the raw file; removed in sanitized copy.

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

