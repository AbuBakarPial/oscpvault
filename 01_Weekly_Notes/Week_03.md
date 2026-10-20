# Week 3 — Networking I: OSI/TCP Models, IP Addressing & Subnetting

**Phase:** Phase 0 — Foundations

Goal: Trace packet movement, calculate CIDR subnets (/24, /16, /26) by hand.

**First Principles:** TCP handshake: SYN → SYN-ACK (open) or RST (closed) → ACK. `/24` subnet = 2^(32-24)=256 addresses, 254 usable. On exam, a dual-homed box with `172.16.50.10/24` → up to 253 other hosts possible.

**Mon/Wed/Fri:** TryHackMe free rooms (What is Networking, Intro to LAN), Professor Messer N10-009 OSI/TCP/Subnetting videos.
**Weekend:** Drill subnetting.net / subnetting-questions.com until splitting a /24 into 4 equal /26s on paper takes <2min.

**References:** Professor Messer Network+ · Subnetting.net

---
*Enforce 2h/3h cap if Week ≥ 11. Update `00_Status/status.md` at session end.*
