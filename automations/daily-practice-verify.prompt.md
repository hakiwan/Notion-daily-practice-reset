Follow @notion-daily-reset.md. This is the **23:59 GMT-3 verify** run.

## Scope

Only read and log **Daily Practice** checkboxes in the Life Areas **Areas** database. Do not modify any Notion properties.

## Notion targets (from discovery)

- **Second Brain page:** `b93bd07d-cbb8-82ba-91d7-811c250d1086`
- **Areas data source:** `collection://831bd07d-cbb8-8380-a905-0738bbf5dac1`
- **Checkbox property:** `Daily Practice` (`__YES__` = checked, `__NO__` = unchecked)

## Steps

1. Use Notion MCP.
2. Search within the Areas data source:
   - `data_source_url`: `collection://831bd07d-cbb8-8380-a905-0738bbf5dac1`
   - `query`: `area`
   - `page_size`: 25
3. For each result page, `notion-fetch` the page and read the `Daily Practice` property from `<properties>`.
4. Build a verify log for today (GMT-3 timestamp) listing:
   - All pages with **Daily Practice** checked (title + page ID + URL)
   - Count of checked vs unchecked
5. Append to `notion-plan-logs.md` under `## Verify YYYY-MM-DD`.

## Restrictions

- Do not modify any Notion properties.
- Do not commit or push `notion-plan-logs.md` (gitignored).
- If blocked for more than 2 minutes, stop and report the error.
