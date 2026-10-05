# Tools Used in Game QA & LQA

> You already know JIRA, Git, TestRail. Here's how the game industry maps to those —
> and what's new.

---

## 🐛 Bug Tracking Tools

### Tools you already know
| Tool | Used in Game QA? |
|---|---|
| **JIRA** | Yes — widely used at studios and service providers |
| **Azure DevOps** | Occasionally, at Microsoft-adjacent studios |
| **TestRail** | Yes — especially at larger QA departments |

### Game-specific bug trackers
| Tool | Notes |
|---|---|
| **DevTrack** | Common at Keywords Studios and similar LQA providers |
| **Hansoft** | Project management + bug tracking, popular at large studios |
| **Mantis Bug Tracker** | Open-source, used at some indie/mid-size studios |
| **Perforce Helix** | Often used for version control + sometimes issue tracking |
| **Internal proprietary tools** | Many large publishers (EA, Ubisoft) use their own systems |

> 💡 If you've used JIRA, you can learn any bug tracker in a day. The concepts are identical —
> tickets, fields, workflow states, attachments, filters.

---

## 🎮 Game Platforms & Hardware

### PC (Windows/Mac)
- Standard keyboard + mouse testing
- Builds delivered as executables or via launchers (Steam, Epic, internal)
- No devkit needed — standard hardware

### Console Devkits
| Platform | Devkit Name | Notes |
|---|---|---|
| PlayStation 5 | PS5 DevKit | Specialized hardware, needs SIES access |
| Xbox Series X/S | Xbox Dev Kit | Similar to retail but with debug features |
| Nintendo Switch | Nintendo DevKit | Strict NDA, access limited |
| PS4 / Xbox One | Previous gen devkits | Still common for cross-gen projects |

> 💡 You won't need to source these yourself — the studio provides them. But knowing they exist
> and how they differ from retail hardware shows you've done your homework.

### What makes devkits different from retail consoles?
- Can run **unsigned / in-development builds** (retail consoles can't)
- Have **debug overlays** showing memory, FPS, build version
- Connected to **bug tracker directly** in some pipelines
- May crash more often — that's expected on pre-release builds

---

## 🌐 Localization Tools (Good to Know, Not Always Required)

### CAT Tools (Computer-Assisted Translation)
LQA testers generally don't *use* these — translators do. But knowing what they are helps:

| Tool | Notes |
|---|---|
| **SDL Trados Studio** | Industry standard CAT tool |
| **memoQ** | Common alternative to Trados |
| **Phrase (formerly Memsource)** | Cloud-based, growing in game localization |
| **Lokalise** | Popular for mobile/indie games |
| **XTM** | Enterprise cloud CAT |

> 💡 As an LQA tester, you'll work from **exported spreadsheets or in-game builds**, not CAT tools directly.

### Reference Tools You Will Use
| Tool | Purpose |
|---|---|
| **Excel / Google Sheets** | Translation reference spreadsheets, bug tracking supplements |
| **PowerPoint / Confluence** | Style guides, glossaries, onboarding docs |
| **FRAPS / OBS / Xbox Game Bar** | Screen recording for subtitle sync bugs |
| **ShareX** | Free screenshot tool with annotation |
| **Discord** | Internal team comms at many studios |

---

## 📸 Screenshot & Video Capture

| Tool | Platform | Free? |
|---|---|---|
| **Xbox Game Bar** (Win+G) | Windows | ✅ Built-in |
| **OBS Studio** | Windows/Mac/Linux | ✅ Free |
| **ShareX** | Windows | ✅ Free |
| **FRAPS** | Windows | Paid (old but reliable) |
| **PS5 built-in capture** | PlayStation | ✅ Built-in |
| **Xbox built-in capture** | Xbox | ✅ Built-in |

> 💡 For subtitle sync bugs, you **must** submit a video. Practice capturing and trimming clips efficiently.

---

## 🔧 Practice Setup (No Devkit Needed)

To practice LQA workflows at home:

1. **Play any AAA game** in Portuguese (change language in settings)
2. **Find real bugs** — truncated text, wrong grammar, missing subtitles
3. **Document them** using the template in [`03-bug-reporting/`](../03-bug-reporting/)
4. **Build a portfolio** of practice bug reports → [`07-portfolio/`](../07-portfolio/)

Good games to practice with (available in PT-BR/PT-PT):
- Any Ubisoft game (Assassin's Creed series)
- Any EA game (FIFA, The Sims)
- Square Enix RPGs (Final Fantasy series)
- Bandai Namco titles
