# AI News Digest — Workflow Instructions

This repo stores daily AI news digests compiled by a scheduled Claude Code task.

## Branch and PR convention

Every run must follow this pattern — do not push directly to `main`:

1. **Create a dated branch** from `main`:
   ```
   git fetch origin main
   git checkout -b ai-digest/YYYY-MM-DD origin/main
   ```
2. **Write the digest** to `ai-digest-YYYY-MM-DD.md` in the repo root.
3. **Commit and push** the dated branch:
   ```
   git add ai-digest-YYYY-MM-DD.md
   git commit -m "Add AI news digest for YYYY-MM-DD"
   git push -u origin ai-digest/YYYY-MM-DD
   ```
4. **Open a PR** from `ai-digest/YYYY-MM-DD` → `main` titled:
   `AI Digest — YYYY-MM-DD`

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
