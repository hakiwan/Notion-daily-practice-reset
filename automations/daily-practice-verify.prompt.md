Follow @notion-daily-reset.md. This is the **23:59 GMT-3 verify** run.

## Scope

Only read and log **Daily Practice** checkboxes in the Life Areas **Areas** database. Do not modify any Notion properties.

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
3. For each result page, `notion-fetch` the page and read the `Daily Practice` property from `<properties>`.
4. Build a verify log for today (GMT-3 timestamp) listing:
   - All pages with **Daily Practice** checked (title + page ID + URL)
   - Count of checked vs unchecked
5. Append to `notion-plan-logs.md` under `## Verify YYYY-MM-DD`.
6. Commit and push the log update to `hakiwan/Notion-daily-practice-reset`.

## Restrictions

- Do not change anything in Notion except appending to the log file in git.
- If blocked for more than 2 minutes, stop and report the error.
