# Master Bibliography

| Category | Resource | URL |
|---|---|---|
| Official Syllabus | OffSec OSCP+ Body of Knowledge | help.offsec.com/hc/en-us/articles/38543335188756 |
| Study Schedules | PEN-200 24-Wk / 12-Wk Plans | help.offsec.com/hc/en-us/articles/15545672357780 / 15541765522196 |
| Exam Rules | OffSec Exam Guide & FAQ | help.offsec.com |
| Linux | Linux Journey, OverTheWire Bandit | linuxjourney.com, overthewire.org/wargames/bandit |
| Networking | Professor Messer Network+, Nmap Book | professormesser.com, nmap.org/book |
| Web/SQLi | PortSwigger Web Security Academy | portswigger.net/web-security |
| Metasploit | OffSec Metasploit Unleashed | offsec.com/metasploit-unleashed |
| PrivEsc | GTFOBins, LOLBAS | gtfobins.github.io, lolbas-project.github.io |
| AD | Hacker Recipes, WADComs, BadBlood, GOAD | thehacker.recipes, wadcoms.github.io, github.com/davidprowe/BadBlood, github.com/Orange-Cyberdefense/GOAD |
| Writeups | HackTricks, IppSec, 0xdf | book.hacktricks.wiki, youtube.com/@ippsec, 0xdf.gitlab.io |

## Exam Day Protocol (24h)
1. Hour 0–1: Triage, proctor check-in, start Nmap scans on 3 standalones, begin AD enum with given creds.
2. Hour 1–9: AD push (MS01→MS02→DC). Time-box roadblocks 90–120min; pivot to standalone 2h if stuck.
3. Hour 9–18: Rotate 3 standalones in 2h blocks, local.txt then proof.txt, until 70+ pts.
4. Rest: 10min break/2.5h; main sleep block after crossing 70pts or after 2 consecutive 90min stalls.
5. Final 2h: Stop new exploits. Verify every flag + screenshot (whoami, ip a/ipconfig, hostname, flag visible, uncropped).

## LainKusanagi PG Practice List (by category)
- **AD/Domain:** Access, Resourced, Nagoya, Hokkaido, Hutch, Vault, Heist, Shenzi
- **Windows Standalone:** Kevin, Internal, Authby, nickel, slort, Hepet, Splodge, wombo, Algernon, Jacko, Craft, Squid, Medjed, DVR4, Mice, Monster, Padlock
- **Linux/Web/SQLi:** hetemit, payday, uc404, butch, morbo, Nibbles, shifty, Nukem, reconstruction, xposedapi, Apex, hawat, pebbles, megavolt, Phobos, Twiggy, billyboss, escape, ClamAV, Pelican, Bratarina

Reserve Hutch, Vault, Heist, Resourced unseen for Week 36 gate mock.
