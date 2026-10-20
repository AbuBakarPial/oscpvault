# OSCP+ Exam Rules, Scoring & Budget

## Scoring (70 to pass)
- AD Set (40 pts, assumed breach): 2 clients/servers + 1 DC. Given valid low-priv domain user at start. 10/10/20 pts.
- 3 Standalone machines (60 pts, 20 each): 10 pts local.txt, 10 pts proof.txt.
- No bonus points. Highest-probability path: Full AD (40) + 1 Full Standalone (20) + 1 Standalone initial (10) = 70.
- Time: 23h45m VPN access, then 24h to submit PDF report.

## Strict Prohibitions
- Zero AI usage (ChatGPT, Claude, Gemini, Copilot, local models, browser AI ext) → immediate revocation.
- Banned: sqlmap, Nessus, OpenVAS, Acunetix, Burp Suite Pro Active Scanner.
- Metasploit exploit/post modules + Meterpreter: only 1 target machine for entire exam. msfvenom non-Meterpreter shells + multi/handler: allowed on all machines.
- No LLMNR/NBT-NS poisoning (Responder), no ARP spoofing.

## Scope Note
AWS cloud NOT tested — skip pre-exam. sqlmap/Nessus taught conceptually in course but banned on exam; do SQLi and vuln verification manually.

## Staged Budget
| Stage | Weeks | Cost | What |
|---|---|---|---|
| 1 Free Mastery | 1–31 | $0 | Linux Journey, Bandit, PortSwigger, THM free, PG Play, local VMs |
| 2 Pre-Gate Sprint | 32–36 | $19 | 1mo PG Practice, real OffSec boxes, 24h gate mock |
| 3A Lean Paid | 37–49 | ~$1,768 | PEN-200 90-day + 1mo PG Practice + 1 attempt |
| 3B High-Slack | 37–49+ | ~$2,768 | Learn One 365-day + 2 attempts |

## Gate Rule (Week 36)
Below 70/100 on the mock → do NOT buy PEN-200. Spend another $19 month drilling the weak category, re-run mock.
