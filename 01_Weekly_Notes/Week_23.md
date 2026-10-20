# Week 23 — Windows Privilege Escalation

**Phase:** Phase 1B — Privilege Escalation

PEN-200: Windows Privilege Escalation (modern Server 2019/2022 tooling).

Token privileges (`whoami /priv`): SeImpersonate/SeAssignPrimaryToken → GodPotato / PrintSpoofer. SeBackupPrivilege → dump SAM/SYSTEM hives, extract local Admin NTLM via impacket-secretsdump.
Service misconfigs: WinPEASx64/SharpUp/icacls/sc.exe — weak binary perms, weak service ACLs, unquoted paths, DLL hijacking.
Scheduled tasks & stored creds: ConsoleHost_history.txt, Unattend.xml, cmdkey /list, AutoLogon registry. Found creds → RunasCs.exe.

See `02_Cheatsheets/02_PrivEsc_Linux_Windows.md` for full command set.

**References:** LOLBAS · HackTricks Windows PrivEsc · GodPotato GitHub · RunasCs GitHub

---
*Enforce 2h/3h cap if Week ≥ 11. Update `00_Status/status.md` at session end.*
