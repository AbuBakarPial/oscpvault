# Week 27 — Domain Enumeration & BloodHound

**Phase:** Phase 1C/1D — Active Directory Mastery

PEN-200: AD Introduction & Enumeration. 40% of exam. Train from a low-priv domain user against local BadBlood/GOAD-Mini (16GB) or GOAD-Light/Full GOAD (24–32GB+).

Test creds across domain machines with NetExec (nxc smb/winrm/mssql), enumerate shares/users, collect graph data (bloodhound-python remote or SharpHound.exe domain-joined). Mark starting user Owned in BloodHound, analyze shortest paths/delegations/ACLs (ForceChangePassword, GenericAll, GenericWrite, WriteDacl).

---
*Enforce 2h/3h cap if Week ≥ 11. Update `00_Status/status.md` at session end.*
