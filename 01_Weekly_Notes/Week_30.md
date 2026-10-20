# Week 30 — Post-Compromise Dumping & Lateral Movement

**Phase:** Phase 1C/1D — Active Directory Mastery

PEN-200: Lateral Movement in AD.

On Admin/SYSTEM for Machine 1/2: dump SAM hashes, LSA secrets, LSASS (impacket-secretsdump or nxc smb --lsa). Move laterally:
- Pass-the-Hash: evil-winrm -H, impacket-wmiexec -hashes, impacket-psexec -hashes
- Overpass-the-Hash/Pass-the-Ticket: Rubeus.exe, export KRB5CCNAME=...
- WMI/WinRM/DCOM/VSS (vssadmin/diskshadow) extraction of NTDS.dit

**References:** The Hacker Recipes (AD) · WADComs · BadBlood GitHub · GOAD Lab

---
*Enforce 2h/3h cap if Week ≥ 11. Update `00_Status/status.md` at session end.*
