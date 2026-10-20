# Week 20 — Linux Privilege Escalation

**Phase:** Phase 1B — Privilege Escalation

PEN-200: Linux Privilege Escalation. Initial access = 10pts; privesc = second 10pts.

Manual audit first: `id`, `sudo -l` (check every allowed binary on GTFOBins + LD_PRELOAD/env_keep), `/etc/passwd` perms, history files, hidden SSH keys.
SUID/SGID + capabilities: `find / -perm -4000 2>/dev/null`, `getcap -r / 2>/dev/null` (e.g. cap_setuid+ep on Python/Perl).
Cron + pspy64: inspect `/etc/crontab`, `/etc/cron.d/`, run pspy64 to watch root procs live — writable scripts, relative paths (PATH hijack), wildcard expansion.
Internal services: `ss -tulpn` bound to 127.0.0.1 as root, then LinPEAS to catch misses.

**Practice:** THM Linux PrivEsc + Linux PrivEsc Arena. Configure a vulnerable SUID binary/cron job/sudo rule on your own VM and audit it. Root 2 free PG Play Linux boxes (3h cap each).

**References:** GTFOBins · HackTricks Linux PrivEsc · OffSec Recordings Weeks 4A–6A

---
*Enforce 2h/3h cap if Week ≥ 11. Update `00_Status/status.md` at session end.*
