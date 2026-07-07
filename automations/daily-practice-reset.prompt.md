Follow @notion-daily-reset.md. This is the **00:01 GMT-3 reset** run.

## Scope

Only uncheck **Daily Practice** on Life Areas pages where it is currently checked. Do not modify any other Notion properties or content.

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
3. For each result page, `notion-fetch` and check `Daily Practice`.
4. For every page where `Daily Practice` is `__YES__`, call `notion-update-page`:
   - `command`: `update_properties`
   - `properties`: `{ "Daily Practice": "__NO__" }`
   - Update **only** that property.
5. Report which pages were reset (title + page ID) and any errors.

## Restrictions

- Do not change anything beyond unchecking **Daily Practice**.
- Do not commit or push anything to GitHub.
- If blocked for more than 2 minutes, stop and report the error.
