# Week 1 — Linux Fundamentals I: Filesystem, Users & Permissions

**Phase:** Phase 0 — Foundations

Goal: Navigate any Linux server blind via terminal, read/edit files, decode rwx permission bits.

**First Principles:** Linux starts at `/`. Key folders: `/etc` (passwd=users, shadow=hashes, crontab=scheduled tasks, sudoers=admin rights), `/var/www` (web files/DB config), `/tmp` & `/dev/shm` (world-writable).
`ls -la` → `-rwxr-xr-- 1 root www-data`: type, then User/Group/Other perms (r=4,w=2,x=1).

**Mon/Wed/Fri (2h each):** Linux Journey — Grasshopper track, start Novice.
**Weekend (4–6h):** OverTheWire Bandit 0–10 (`ssh bandit0@bandit.labs.overthewire.org -p 2220`). No searching solutions — use `man find`, `man file`.

**Commands:** ls -la, cd, pwd, cat, less, head, tail, file, find, locate, chmod, chown, id, whoami, man, which

**References:** Linux Journey · OverTheWire Bandit

---
*Enforce 2h/3h cap if Week ≥ 11. Update `00_Status/status.md` at session end.*
