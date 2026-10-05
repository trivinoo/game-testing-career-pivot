# Software QA vs. Game QA — Parallels & Differences

> You already know more than you think. This document maps your existing skills
> and highlights only what's genuinely new.

---

## 🔁 The Core Loop Is the Same

Both disciplines follow the same fundamental cycle:

```
Understand expected behavior
        ↓
Execute tests / play through content
        ↓
Identify deviations from expected behavior
        ↓
Document them (bug report)
        ↓
Retest after fix (regression)
```

The **domain** changes. The **mindset** doesn't.

---

## 📊 Side-by-Side Comparison

| Dimension | Software QA | Game QA |
|---|---|---|
| **Test artifact** | Application feature, API, UI | Game build (PC, console, mobile) |
| **Bug tracker** | JIRA, Azure DevOps, TestRail | JIRA, DevTrack, Mantis, internal tools |
| **Test basis** | Requirements spec, user stories | Game Design Document (GDD), style guides |
| **Regression** | Run regression suite on new build | Re-test fixed bugs on new build (same concept) |
| **Environment** | Browser, OS, server | Console (PS5, Xbox, Switch), PC, devkit |
| **Severity levels** | Critical / High / Medium / Low | Blocker / Critical / Major / Minor / Cosmetic |
| **Collaboration** | Devs, PMs, designers | Localization PMs, translators, audio engineers, devs |
| **Daily routine** | Exploratory + scripted testing | Play assigned sections + follow test checklist |

---

## 🆕 What's Genuinely New in Game QA

### 1. Game-specific bug types
- **Truncation** — text cut off due to UI box size
- **Lip-sync mismatch** — audio doesn't match character mouth movement
- **Missing/empty string** — untranslated placeholder in target language
- **Subtitle sync** — subtitle appears too early/late vs audio
- **Context mismatch** — translation is technically correct but wrong for the in-game situation
- **Hardcoded text** — text that can't be localized (needs dev fix)
- **Font issues** — special characters (ã, ç, õ) render incorrectly or are missing

### 2. Working with game builds
- Builds are often unstable — crashes are expected and not always "your" bug
- You'll get access via **devkits** (console dev hardware) or PC clients
- Build notes / changelogs tell you what changed — read them every morning

### 3. Localization-specific context
- You're testing **translated content**, not original
- You need to catch errors the translator might not have noticed in context
- Source text (usually English) is your reference — you compare against it

### 4. Style guides and glossaries
- Every major game/publisher has a **style guide** (tone, formality register, punctuation rules)
- **Glossary** = approved translations for key terms (character names, items, abilities)
- Deviating from the glossary = a reportable bug even if linguistically correct

---

## ✅ What You Don't Need to Learn from Scratch

- Bug lifecycle (open → in progress → fixed → verified → closed)
- How to write a reproducible bug report
- Test planning and prioritization
- Communicating with devs about unclear expected behavior
- Managing multiple tasks and deadlines
- Reading changelogs and build notes
- Using bug tracking systems

---

## 🎯 Key Takeaway

> **Game QA is software QA with a controller in your hand and a style guide on your desk.**
> Your 3+ years of experience make you a stronger candidate than most entry-level applicants.
> The gap to close is domain vocabulary and localization-specific bug types — both learnable in weeks.
