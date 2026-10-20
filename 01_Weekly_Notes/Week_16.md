# Week 16 — Directory Traversal & LFI

**Phase:** Phase 1A — Recon, Web & Manual SQLi

PEN-200: Common Web App Attacks (Part 1).
Stepping out of web root (`../../../../etc/passwd`), PHP stream wrappers (`php://filter/convert.base64-encode/resource=index.php`) to read source, Log Poisoning (inject PHP via User-Agent header, include access.log via LFI → RCE).

---
*Enforce 2h/3h cap if Week ≥ 11. Update `00_Status/status.md` at session end.*
