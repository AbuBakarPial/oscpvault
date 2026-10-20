# Week 2 — Linux Fundamentals II: Processes, Cron, Pipes & Redirection

**Phase:** Phase 0 — Foundations

Goal: Chain commands with pipes, suppress errors, inspect processes, understand scheduled tasks.

**First Principles:** 3 streams — 0 stdin, 1 stdout, 2 stderr. `|` pipes Command A output into Command B input. `2>/dev/null` hides errors.

**Mon/Wed/Fri:** Finish Novice, complete Journeyman track on Linux Journey (processes, packages, network files, cron).
**Weekend:** Bandit 10–20 (base64, hex, compression, SSH private keys, `nc`).

**Checkpoint commands to master & explain:**
```
find / -writable -type f -not -path "/proc/*" 2>/dev/null
grep -rnw '/var/www/' -e 'password' 2>/dev/null
ps aux && ss -tulpn && crontab -l
```

---
*Enforce 2h/3h cap if Week ≥ 11. Update `00_Status/status.md` at session end.*
