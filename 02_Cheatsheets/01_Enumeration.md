# Enumeration Cheatsheet

> Grows weekly. Start filling Week 13–14.

## Nmap 3-Stage Routine
```
nmap -p- --min-rate 3000 -oN all_ports $IP
nmap -p<ports> -sC -sV -O -oN targeted $IP
nmap -sU --top-ports 100 -oN udp $IP
```

## DNS (53)
```
dig axfr @$IP domain.local
ffuf -w subdomains.txt -u http://FUZZ.domain.local
```

## SMB (139/445)
```
nxc smb $IP -u '' -p '' --shares
smbclient -N -L //$IP
enum4linux-ng $IP
```

## SNMP (UDP 161)
```
onesixtyone -c community.txt $IP
snmpwalk -v2c -c public $IP
```

## NFS (2049) / SMTP (25)
```
showmount -e $IP
# SMTP VRFY/EXPN for user enum
```

## Web Dirs
```
gobuster dir -u http://$IP -w /usr/share/seclists/...
feroxbuster -u http://$IP -w wordlist
```

## Checkpoint Commands
```
find / -writable -type f -not -path "/proc/*" 2>/dev/null
grep -rnw '/var/www/' -e 'password' 2>/dev/null
ps aux && ss -tulpn && crontab -l
```
