# Week 29 — AD Authentication, Password Spraying, Kerberos & ACL Attacks

**Phase:** Phase 1C/1D — Active Directory Mastery

PEN-200: Attacking AD Authentication.

**Week 28:** NTLM vs Kerberos (KDC/TGT/TGS). Credential storage: LSASS, SAM, LSA Secrets, NTDS.dit. Password spray: `nxc smb $DC_IP -u users.txt -p 'Password123' --continue-on-success`.

**Week 29:** Sync clock (`sudo ntpdate $DC_IP`). AS-REP Roast (impacket-GetNPUsers → hashcat -m18200). Kerberoast (impacket-GetUserSPNs → hashcat -m13100). ACL abuse (bloodyAD/net rpc on GenericAll/GenericWrite). Silver tickets & DCSync (impacket-secretsdump).

See `02_Cheatsheets/04_Active_Directory.md` for full command sequence.

---
*Enforce 2h/3h cap if Week ≥ 11. Update `00_Status/status.md` at session end.*
