# OSCP+ 49-Week Vault

Shared vault. Both brothers clone same GitHub repo, open folder as Obsidian vault.

## Structure
- `00_Status/status.md` — AI-continuity log. Update every session: current week, last done, next action, blockers.
- `01_Weekly_Notes/` — One file per week (Week_01.md … Week_49.md). Phase, goal, tasks, references, checkpoint.
- `02_Cheatsheets/` — Shared, grows as you progress: Enumeration, Linux PrivEsc, Windows PrivEsc, Web, AD, Tunneling, File Transfer.
- `03_Templates/` — Box_Template.md (per-machine writeup), Topic_Template.md (per-concept note).
- `04_Reference/` — Master bibliography, exam rules, scoring, budget stages.
- `docs/index.html` — The full 49-week reference textbook, styled as a live site. Served via GitHub Pages.

## Workflow
1. `git init`, push to repo (public, for free GitHub Pages).
2. Both open vault folder in Obsidian.
3. Each session start: update `status.md`.
4. Each box rooted: copy `Box_Template.md` into `01_Weekly_Notes/boxes/`, fill in.
5. New technique learned → add to relevant cheatsheet in `02_Cheatsheets/`.
6. Sunday: debrief, clean notes, 2-sentence failure log entry if stuck >3h.

## GitHub Pages (live site)
Repo Settings → Pages → Source: `Deploy from branch` → Branch: `main` → Folder: `/docs` → Save.
Live at `https://<username>.github.io/<repo>/` in ~1 min.

## Rules (standing, Weeks 11–48)
2h independent → 1 hint → 3h hard stop → read writeup, log lesson, move on.
