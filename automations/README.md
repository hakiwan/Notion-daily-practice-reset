# Cursor Automations — Daily Practice Reset

Two scheduled automations for `hakiwan/Notion-daily-practice-reset`.

| Automation | Local time (GMT-3) | UTC cron | Prompt file |
|------------|-------------------|----------|-------------|
| Daily Practice Verify | 23:59 | `59 2 * * *` | [daily-practice-verify.prompt.md](./daily-practice-verify.prompt.md) |
| Daily Practice Reset | 00:01 | `1 3 * * *` | [daily-practice-reset.prompt.md](./daily-practice-reset.prompt.md) |

## Shared settings

- **Repo:** `hakiwan/Notion-daily-practice-reset`
- **Tools:** Notion MCP (`notion`)
- **Spec:** `@notion-daily-reset.md`
- **Logs:** `@notion-plan-logs.md`

## Setup in Cursor (Agents Window)

1. Open **Automations** in Cursor.
2. Create **Daily Practice Verify**:
   - Trigger: cron `59 2 * * *` (23:59 Brasília / GMT-3)
   - Repo: `hakiwan/Notion-daily-practice-reset`
   - Tools: Notion MCP
   - Instructions: paste contents of `automations/daily-practice-verify.prompt.md`
3. Create **Daily Practice Reset**:
   - Trigger: cron `1 3 * * *` (00:01 Brasília / GMT-3)
   - Repo: `hakiwan/Notion-daily-practice-reset`
   - Tools: Notion MCP
   - Instructions: paste contents of `automations/daily-practice-reset.prompt.md`

Both automations require Notion MCP to be authenticated in Cursor.
