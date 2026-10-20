# Week 19 — Password Attacks, Locating & Fixing Public Exploits

**Phase:** Phase 1A — Recon, Web & Manual SQLi

PEN-200: Password Attacks, Locating Public Exploits, Fixing Exploits.

- Network login auditing: Hydra + Burp Intruder on SSH/FTP/RDP/HTTP POST — avoid lockouts.
- Offline hash cracking: hashid, Hashcat (MD5, Linux SHA-512/yescrypt, NTLM -m1000, Net-NTLMv2 -m5600), rockyou.txt + best64.rule.
- Adapting broken exploits: searchsploit, read PoC before running, fix hardcoded URL/port/shellcode, Py2→Py3, cross-compile Windows C exploits (`x86_64-w64-mingw32-gcc exploit.c -o exploit.exe -lws2_32`).

**References:** Hashcat Wiki · SearchSploit Docs

---
*Enforce 2h/3h cap if Week ≥ 11. Update `00_Status/status.md` at session end.*
