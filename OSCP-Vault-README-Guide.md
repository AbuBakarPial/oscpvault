<div align="center">

# ⚔️ OSCP+ VAULT — The 49-Week Field Manual

**Two brothers. Zero IT background assumed. One certification.**
**Enumerate → Exploit → Escalate → Document → Repeat**

[![Live Textbook](https://img.shields.io/badge/📖_LIVE_TEXTBOOK-Open_Site-00c853?style=for-the-badge)](https://abubakarpial.github.io/oscpvault/)
![Weeks](https://img.shields.io/badge/PLAN-49_WEEKS-blue?style=for-the-badge)
![Hours](https://img.shields.io/badge/RHYTHM-10–14_H%2FWEEK-orange?style=for-the-badge)
![Start Cost](https://img.shields.io/badge/START_COST-$0-brightgreen?style=for-the-badge)
![Pass Mark](https://img.shields.io/badge/PASS-70%2F100-red?style=for-the-badge)

</div>

> [!IMPORTANT]
> **The live textbook is the full guide:** **[abubakarpial.github.io/oscpvault](https://abubakarpial.github.io/oscpvault/)** — 12 chapters, searchable, works on phone. This README is the *operating manual*: how to start, how the repo works, how Obsidian fits in, and how to run the 49 weeks.

---

## 📑 Contents

- [🚀 Start Here — Day 1](#-start-here--day-1-in-this-exact-order)
- [🗂️ What Is This Repo?](#️-what-is-this-repo)
- [📅 The Full 49-Week Study System](#-the-full-49-week-study-system)
- [🧠 How To Study Each Week](#-how-to-study-each-week)
- [💎 Obsidian Setup & Templates](#-obsidian-setup--templates)
- [🔄 Updating The Repo From Obsidian](#-updating-the-repo-from-obsidian)
- [👥 Two-Brother Workflow](#-two-brother-workflow)
- [⛔ Exam Rules You Train By](#-exam-rules-you-train-by)
- [📊 Progress Tracking](#-progress-tracking)

---

## 🚀 Start Here — Day 1, In This Exact Order

| Step | Do this | Done when |
|---|---|---|
| **1** | Clone this repo (see [Obsidian Git setup](#-updating-the-repo-from-obsidian) — or `git clone https://github.com/AbuBakarPial/oscpvault.git`) | The folder sits on your PC |
| **2** | Open the folder as a vault in **Obsidian** → Settings → enable the **Templates** core plugin → set template folder to `03_Templates` | Obsidian shows all folders |
| **3** | Open **`00_Status/status.md`** and fill it in: Week `1`, Phase `0 — Foundations`, your name in *Who* | Status log is alive |
| **4** | Set up your lab using **Chapter 03** of the [live textbook](https://abubakarpial.github.io/oscpvault/) (Kali VM + RAM sizing) | Kali boots, terminal works |
| **5** | Open **`01_Weekly_Notes/Week_01.md`** and start: Linux Journey (Grasshopper) + OverTheWire Bandit 0–10 this weekend | Week 1 tasks ticking off |
| **6** | End of session: update `status.md` (last done / next action / blockers), then **sync the repo** (pull → commit → push) | Your brother sees your progress |

> [!TIP]
> Don't read all 49 weeks first. Read **this week's file + the textbook chapter it points to**, nothing more. The plan only works one week at a time.

---

## 🗂️ What Is This Repo?

One shared brain for two people: an **Obsidian vault** and a **published textbook site**, in a single repo.

| Path | What it is | Rule |
|---|---|---|
| `00_Status/status.md` | 🧭 **AI-continuity log** — current week, last done, next action, blockers | Update at **every** session start/end |
| `01_Weekly_Notes/Week_01.md` … `Week_49.md` | 📅 One file per week: phase, goal, tasks, commands, references, checkpoint | Work top-to-bottom, one week at a time |
| `01_Weekly_Notes/boxes/` | 🖥️ One write-up per rooted machine (from the Box Template) | Every rooted box gets a file. No exceptions |
| `02_Cheatsheets/` | ⚡ Your personal, growing cheatsheets (5 files — see growth schedule below) | Every new technique you learn lands here |
| `03_Templates/` | 📝 `Box_Template.md` + `Topic_Template.md` | Never edit the originals — always copy/insert |
| `04_Reference/` | 📚 Exam rules & scoring, master bibliography | Read before Stage 2 and again before exam day |
| `docs/index.html` | 🌐 The full 49-week textbook website (GitHub Pages source) | Edit → push → site updates in ~1 minute |

**Cheatsheet growth schedule** — they are skeletons on purpose, *you* fill them:

| Cheatsheet | Fill during |
|---|---|
| `01_Enumeration.md` | Weeks 13–14 |
| `03_Web_And_SQLi.md` | Weeks 15–18 |
| `02_PrivEsc_Linux_Windows.md` | Weeks 20–23 |
| `05_Tunneling_And_File_Transfer.md` | Weeks 3 (file transfer) + 25–26 (tunneling) |
| `04_Active_Directory.md` | Weeks 27–30 |

---

## 📅 The Full 49-Week Study System

### The phases

| Phase | Weeks | Focus | Cost |
|---|---|---|---|
| **0 — Foundations** | 1–12 | Linux, TCP/IP networking, Windows/AD basics, web basics, scripting, first boxes *(Week 12 = buffer)* | $0 |
| **1A — Recon, Web & SQLi** | 13–19 | Service enumeration, LFI/RFI, file uploads, **manual** SQLi, password attacks | $0 |
| **1B — Privilege Escalation** | 20–23 | Linux: SUID, capabilities, cron · Windows: tokens, services, registry | $0 |
| **1C/1D — Pivot & AD** | 24–35 | Ligolo-ng pivoting, Metasploit (exam-legal use), Kerberos, BloodHound, lateral movement *(Week 31 = rest/buffer)* | $0 → $19 |
| **🚪 THE GATE** | 36 | 24-hour blind mock exam + 5-point financial gate test (below) | $19 |
| **2 — Paid Window** | 37–49 | PEN-200 course + labs, LainKusanagi PG Practice list, timed mocks, exam | ~$1,749 |

### The money logic — never risk $1,749 blind

| Stage | Weeks | Cost | What |
|---|---|---|---|
| 1 · Free Mastery | 1–31 | **$0** | Linux Journey, Bandit, PortSwigger Academy, THM free, PG Play, local VMs |
| 2 · Pre-Gate Sprint | 32–36 | **$19** | 1 month PG Practice — real OffSec boxes + the Gate mock |
| 3A · Lean Paid | 37–49 | **~$1,768** | PEN-200 (90-day) + 1 mo PG Practice + 1 exam attempt |
| 3B · High-Slack | 37–49+ | **~$2,768** | Learn One (365-day) + 2 attempts |

### 🚪 The Week 36 Gate — all five, or you don't buy

1. **24h blind mock ≥ 70/100** — brother picks 4 unseen PG Practice boxes (1 AD set + 1 Windows + 2 Linux), strict exam sim, zero hints, full report written.
2. **12–15+ boxes rooted** across free + PG Practice, all under the 3h cap, all written up in Obsidian.
3. **Local AD chain in < 90 min from memory** — low-priv domain user → Domain Admin, incl. Ligolo-ng pivot (BadBlood/GOAD lab).
4. **Manual web fluency** — 5 PortSwigger SQLi + LFI/Upload labs at Practitioner level, **zero sqlmap**.
5. **Core mechanics from muscle memory** — TTY upgrade, file transfers (3 protocols, Linux + Windows), Ligolo-ng tunnel — no syntax lookups.

> [!WARNING]
> **Gate Rule:** Mock below 70 → **do NOT buy PEN-200.** Spend another $19 month drilling the weak category, then re-run a fresh 4-box mock.

---

## 🧠 How To Study Each Week

**Weekly rhythm — 10–14 hours:**

| When | Time | What |
|---|---|---|
| Mon / Wed / Fri | 2h each | The week's guided material (course, labs, reading) from that week's file |
| Weekend | 4–6h | Hands-on: boxes, Bandit/PortSwigger labs, write-ups |
| Sunday | 30 min | Debrief: clean notes, update cheatsheets, update `status.md`, sync repo |

**Every session runs the same loop:**

```
1. PULL      → sync the repo first (get your brother's latest)
2. STATUS    → open 00_Status/status.md — where did we stop? what's next?
3. STUDY     → work this week's file + linked textbook chapter
4. CAPTURE   → new technique? → cheatsheet. New concept? → Topic Template note.
               Box rooted? → Box Template write-up in 01_Weekly_Notes/boxes/
5. LOG       → stuck >3h? write the 2-sentence failure log entry
6. PUSH      → update status.md, commit, push. Done.
```

> [!CAUTION]
> **The standing anti-rabbit-hole rule (Weeks 11–48):**
> **2 hours independent → 1 hint → 3 hours hard stop → read the writeup → log the lesson → move on.**
> Time you burn past 3 hours is time stolen from the next topic. The exam is 24 hours — pacing *is* the skill.

**Two tracks, one plan (Weeks 1–12):** the developer brother and the true-beginner brother follow the *same* weekly files. The beginner reads **Chapter Zero** of the textbook first (how computers & networks actually work); the developer skips ahead to the tasks and pairs up for the weekend boxes. Nobody waits, nobody gets left behind.

---

## 💎 Obsidian Setup & Templates

### One-time setup (5 minutes)

1. **Open vault:** Obsidian → *Open folder as vault* → select the cloned repo folder.
2. **Templates core plugin:** Settings → Core plugins → **Templates ON** → Templates settings → folder = `03_Templates`.
3. **(Recommended) Daily notes OFF, Templater optional** — the built-in Templates plugin is enough for this vault.
4. **Set a hotkey:** Settings → Hotkeys → *Templates: Insert template* → e.g. `Ctrl+T`.

### 📝 Box Template — for every machine you attack

**When:** the moment you start a box (HTB / THM / PG Play / PG Practice).
**How:** create the file first, fill it *while* you work — not from memory afterwards.

1. New file inside `01_Weekly_Notes/boxes/` named e.g. `PG-Shenzi.md`
2. `Ctrl+T` → insert **Box_Template**
3. Fill the frontmatter as you go:

| Field | Fill with |
|---|---|
| `box` / `platform` | Name + HTB / THM / PG Play / PG Practice |
| `os` | Linux / Windows / AD |
| `difficulty` | Easy / Medium / Hard / Insane |
| `date` / `time_spent` | Date started / total hours (honest number) |
| `hint_used` | `none` / `1 nudge at 2h` / `read writeup at 3h` |

Then work the sections in order — **Enumeration → Foothold → Shell Stabilization → Privilege Escalation → Flags (`local.txt` / `proof.txt`)**. The last section is the point of the whole file:

> **Lesson** — if you were stuck >3h, write exactly 2 sentences: what the blocker was, what the fix pattern is. These lessons feed your cheatsheets.

### 📝 Topic Template — for every concept you learn

**When:** you learn a technique that isn't box-specific (Kerberoasting, SUID abuse, PHP filters…).
**How:** new note (root or the relevant week's folder) → `Ctrl+T` → **Topic_Template** → fill `topic` + `week`, then **Core Concept** (in your own words — if you can't write it, you don't know it), **Commands**, **Common Pitfalls**, **References**.

---

## 🔄 Updating The Repo From Obsidian

Use the **Obsidian Git** plugin — then syncing is one click (or fully automatic) and you never touch a terminal.

### One-time setup (each brother, each PC)

1. Settings → Community plugins → **Turn on community plugins** → Browse → search **"Git"** (by Vinzent) → Install → Enable.
2. Sign in to GitHub once so the plugin can push: on Windows, Git Credential Manager pops a browser login the first time you pull/push; on Mac/Linux, use a GitHub **Personal Access Token** (GitHub → Settings → Developer settings → Tokens (classic) → `repo` scope) as the password when asked.
3. In Obsidian Git settings, set:
   - **Pull on startup:** ON *(this is the big one — you always start from the latest)*
   - **Push after commit:** ON
   - **Auto backup (commit+push) interval:** 10–30 min *(optional safety net)*
   - **Commit message:** leave default, or use `vault: {{date}}`

### Every session after that

| Moment | Action |
|---|---|
| **Start** | Open Obsidian → Git plugin auto-pulls (or Command palette → *Git: Pull*) |
| **During** | Just edit notes normally — templates, write-ups, cheatsheets |
| **Finish** | Command palette (`Ctrl/Cmd+P`) → **Git: Commit-and-sync** |
| **Weekly** | If you also edited `docs/index.html`, the live site rebuilds ~1 min after the push |

<details>
<summary><b>⌨️ No plugin? Manual Git commands (same result)</b></summary>

```bash
# start of session
git pull

# end of session
git add .
git commit -m "week 07: rooted PG box + privesc cheatsheet update"
git push
```
</details>

<details>
<summary><b>📱 No Git at all? GitHub web (emergency only)</b></summary>

Repo page → *Add file → Upload files* → drag the changed files → Commit. Works, but overwrites whole files — never use it for a file your brother may have edited the same day.
</details>

> [!WARNING]
> **Conflict rules for two editors:**
> 1. **Pull before you write. Push when you stop.** 90% of conflicts die right there.
> 2. Never both edit the *same file* on the *same day* without a quick message first — `status.md` is the #1 clash file, so update it last, right before pushing.
> 3. If Git reports a conflict: don't panic, don't delete. Open the file, find the `<<<<<<<` markers, keep the merged truth, delete the markers, commit-and-sync.

---

## 👥 Two-Brother Workflow

| Habit | Why |
|---|---|
| Both clone the **same** repo, both open it as an Obsidian vault | One shared brain — notes are identical everywhere |
| Each session starts by updating `00_Status/status.md` | Any brother (or any AI tool) can pick up exactly where the other stopped |
| Gate mock: one brother **sets** the exam, the other **sits** it | You can't pick boxes you've already seen — that's the whole point of Week 36 |
| Sunday debrief together, notes cleaned together | Messy notes in October become a failed report in exam week |

---

## ⛔ Exam Rules You Train By

- **Scoring:** AD set **40 pts** (assumed breach — you're given a low-priv domain user) + 3 standalone machines **20 pts each** (10 `local.txt` + 10 `proof.txt`). **70/100 passes.** Smartest path: full AD (40) + 1 full standalone (20) + 1 foothold (10) = 70.
- **Time:** 23h 45m of VPN access, then 24h to submit the PDF report.
- **Zero AI on the exam** — no ChatGPT/Claude/Gemini/Copilot, no browser AI extensions. Instant revocation. Train like it: hints come from your cheatsheets, not a chatbot.
- **Banned tools:** sqlmap, Nessus, OpenVAS, Acunetix, Burp Pro active scanner — so all SQLi and vuln checks in this vault are **manual**.
- **Metasploit:** exploit/post modules + Meterpreter on **one** machine only for the whole exam. `msfvenom` (non-Meterpreter) + `multi/handler` are fine everywhere.
- **No** Responder poisoning, **no** ARP spoofing. **AWS is not tested** — don't spend weeks on it.

Full detail: `04_Reference/Exam_Rules_And_Scoring.md` and Chapter 02 of the textbook.

---

## 📊 Progress Tracking

Keep these numbers honest in `00_Status/status.md`:

- **Current week / phase** — where you actually are, not where the calendar says
- **Cumulative boxes rooted:** target **12–15 by Week 36**
- **Buffer used:** Week 12 buffer? Week 31 rest taken? (Use them — that's what they're for)
- **Budget stage:** Stage 1 ($0) → Stage 2 ($19) → Stage 3 (PEN-200) — tick only when you actually move

---

<div align="center">

### 🔗 Links

**[📖 Live Textbook](https://abubakarpial.github.io/oscpvault/)** · **[🗂️ Repo Home](https://github.com/AbuBakarPial/oscpvault)** · **[📚 Table of Contents](https://abubakarpial.github.io/oscpvault/#toc)** · **[⚔️ Phase 0 — Weeks 1–12](https://abubakarpial.github.io/oscpvault/#ch5)**

*Try Harder is not the plan. The plan is the plan — 49 weeks, one week at a time.*

`root@oscpvault:~# ./try-harder`

</div>
