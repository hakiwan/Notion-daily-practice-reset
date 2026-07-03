Follow @notion-daily-reset.md. This is the **00:01 GMT-3 reset** run.

## Scope

Only uncheck **Daily Practice** on Life Areas pages where it is currently checked. Do not modify any other Notion properties or content.

## Notion targets (from discovery)

- **Second Brain page:** `392bd07d-cbb8-806f-b7e0-ce98a9cab0db`
- **Areas data source:** `collection://7a8bd07d-cbb8-824c-8d82-079d94aa845e`
- **Checkbox property:** `Daily Practice` (`__YES__` = checked, `__NO__` = unchecked)

## Steps

1. Use Notion MCP.
2. Search within the Areas data source:
   - `data_source_url`: `collection://7a8bd07d-cbb8-824c-8d82-079d94aa845e`
   - `query`: `area`
   - `page_size`: 25
3. For each result page, `notion-fetch` and check `Daily Practice`.
4. For every page where `Daily Practice` is `__YES__`, call `notion-update-page`:
   - `command`: `update_properties`
   - `properties`: `{ "Daily Practice": "__NO__" }`
   - Update **only** that property.
5. Append to `notion-plan-logs.md` under `## Reset YYYY-MM-DD`:
   - GMT-3 timestamp
   - List of pages reset (title + page ID)
   - Any errors (continue on individual failures)
6. Commit and push the log update to `hakiwan/Notion-daily-practice-reset`.

## Restrictions

- Do not change anything beyond unchecking **Daily Practice**.
- If blocked for more than 2 minutes, stop and report the error.
