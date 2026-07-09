# AI News Digest — Workflow Instructions

This repo stores daily AI news digests compiled by a scheduled Claude Code task.

## Publishing convention

Every run pushes directly to `main` — no branches or PRs:

1. **Pull latest `main`**:
   ```
   git fetch origin main
   git checkout main
   git pull origin main
   ```
2. **Write the digest** to `ai-digest-YYYY-MM-DD.md` in the repo root.
3. **Update the index** in `README.md` by prepending a new row to the index table:
   ```
   | YYYY-MM-DD | [AI Digest — YYYY-MM-DD](ai-digest-YYYY-MM-DD.md) |
   ```
   The newest entry must always be at the top of the table (below the header row).
4. **Commit and push** both files together:
   ```
   git add ai-digest-YYYY-MM-DD.md README.md
   git commit -m "Add AI news digest for YYYY-MM-DD"
   git push origin main
   ```

Use today's date (available in the session context) for all placeholders above.

## Digest format

- Filename: `ai-digest-YYYY-MM-DD.md`
- 5–10 items from the past 24 hours
- Categories: New Framework · New Model · New Agent Tool · Research · Other
- Each item: source link, title, 1–2 sentence summary, why it matters
- If no significant updates, note it briefly in the file

## What to search

Technology portals, forums, Twitter/X, arXiv, and news aggregators for:
- New model releases (open and closed source)
- Framework and tooling announcements
- Agent infrastructure (orchestration, memory, tool use)
- Notable research papers
- Industry moves (funding, acquisitions, policy)
