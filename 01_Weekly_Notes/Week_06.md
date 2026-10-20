# Week 6 — Web Application Basics & Burp Suite Proxy

**Phase:** Phase 0 — Foundations

Goal: Read raw HTTP requests/responses, understand methods/headers/cookies, intercept with Burp Suite Community.

**First Principles:** HTTP is stateless — browser sends plain-text requests (`GET /profile.php HTTP/1.1`). Server issues Session Cookie (`Cookie: PHPSESSID=xyz123`) to track you. Burp sits between browser and server — pause/modify requests mid-flight.

**Mon/Wed/Fri:** THM How the Web Works + Burp Suite: The Basics, PortSwigger intro HTTP pages.
**Weekend:** Deploy DVWA on Docker (`docker run --rm -it -p 80:80 vulnerables/web-dvwa`), route browser through Burp (`127.0.0.1:8080`), practice Burp Proxy + Repeater.

---
*Enforce 2h/3h cap if Week ≥ 11. Update `00_Status/status.md` at session end.*
