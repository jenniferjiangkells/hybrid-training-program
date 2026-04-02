# Hybrid Training System

A personal training planning app for hybrid athletes — built for HYROX, Olympic lifting, and running, using gym classes as fixed anchors.

**Live:** [jenniferjiangkells.github.io/hybrid-training-program](https://jenniferjiangkells.github.io/hybrid-training-program)

## What it does

- **Overview** — weekly non-negotiables, plan builder (drag-and-drop block chain), block structure reference
- **Session Menu** — browse and filter sessions by type and tag, build a weekly plan day by day
- **Weekly Check** — non-negotiable checklist, load check, and green/yellow/red week colour rating
- **Goal Blocks** — detailed breakdown of each training block (A–D) with weekly structure, squat program fit, and goals
- **Squat Programs** — RSP vs velocity-based comparison, pairing matrix, 1RM calculator
- **Running** — Runna plan adjustments per block, interval and long run progressions for Block B
- **References** — program design rationale, training tips, and source links

All state (week plan, block chain, checklist, custom sessions) is saved in `localStorage` — no backend required.

## Files

```
index.html    — the entire app (single file, no build step)
content.md    — plain-text export of all training content
README.md     — this file
```

## Updating training content

All the program details live in `content.md` as clean markdown. The workflow for refining the program:

1. Open `content.md` (or copy a section from it)
2. Paste into [Perplexity](https://www.perplexity.ai) or any AI tool and ask it to refine, restructure, or expand
3. Paste the updated content back here in a Claude Code session
4. Ask Claude to apply the changes to `index.html`

Example prompts:
- *"Here's my updated Block B section — apply it to index.html"*
- *"I changed the interval run progression in content.md, sync it to the HTML"*
- *"Add this new session to the session library"*

Changes to `content.md` alone don't affect the live app — Claude reads the diff and updates `index.html` to match.

## Deploying changes

The app is deployed via GitHub Pages from the `main` branch. To publish updates:

```bash
git add index.html content.md
git commit -m "your message"
git push
```

GitHub Pages will update within ~30 seconds.
