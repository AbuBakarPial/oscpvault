# Week 5 — Windows Internals & Active Directory Lab Construction

**Phase:** Phase 0 — Foundations

Goal: Navigate Windows via CMD/PowerShell, understand Registry/Services, build local BadBlood DC lab.

**Mon/Wed/Fri:** THM Windows Fundamentals 1/2/3 + Active Directory Basics. Learn Users, Groups, OUs, GPOs.
**Weekend Lab (16GB host):** Install Windows Server 2022 Eval VM (4GB RAM), promote to DC (`Install-WindowsFeature AD-Domain-Services`), join Win10/11 client (3–4GB) to domain, run free BadBlood script (`Invoke-BadBlood.ps1`) on DC → thousands of realistic users/groups/SPNs/ACLs for Week 27.

**Commands:** whoami /all, net user, net localgroup administrators, ipconfig /all, sc.exe query, Get-Process, Get-Service

---
*Enforce 2h/3h cap if Week ≥ 11. Update `00_Status/status.md` at session end.*
