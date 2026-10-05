# LQA Bug Report Template

> Adapted from standard software QA bug report format.
> Fields marked ⭐ are mandatory in most LQA trackers.

---

## Bug Report Fields

### ⭐ Title
```
[LANG][CATEGORY] Short, specific description of the issue
```
**Examples:**
- `[PT-BR][SPELLING] "Espada" misspelled as "Espda" in inventory screen`
- `[PT-BR][TRUNCATION] Weapon name cut off in equip menu`
- `[PT-BR][SUBTITLE] Subtitle appears 2 seconds after audio starts — Chapter 3 intro`
- `[PT-BR][MISSING] Main menu "Continue" button shows English text in PT-BR build`

---

### ⭐ Language
`Brazilian Portuguese (PT-BR)` / `European Portuguese (PT-PT)`

---

### ⭐ Bug Category
Choose one:
- `Linguistic` — spelling, grammar, punctuation
- `Consistency` — same term translated differently
- `Context` — correct but wrong for the situation
- `Truncation` — text cut off
- `Overflow` — text outside UI bounds
- `Missing String` — untranslated / empty
- `Subtitle Sync` — timing off
- `Font/Encoding` — character rendering issue
- `Style Guide Violation`
- `Glossary Violation`
- `Hardcoded`

---

### ⭐ Severity
| Level | Description |
|---|---|
| **Blocker** | Prevents testing (game crashes, entire screen untranslated) |
| **Critical** | Major linguistic error visible to all players in a prominent location |
| **Major** | Clear error that impacts comprehension or immersion |
| **Minor** | Noticeable error but meaning still understood |
| **Cosmetic** | Very minor (e.g., extra space, optional style preference) |

---

### ⭐ Steps to Reproduce
```
1. Start a New Game
2. Progress to Chapter 1 — "The Awakening"
3. Trigger the first cutscene (automatically plays after tutorial)
4. Observe the first subtitle line
```

---

### ⭐ Location / Path
```
Main Menu → New Game → Chapter 1: The Awakening → Opening Cutscene → Line 1
```

---

### ⭐ Current Text (What you see)
```
"Eu não posse continuar assim."
```

---

### ⭐ Expected Text (What it should be)
```
"Eu não posso continuar assim."
```

---

### ⭐ Source Text (English original for reference)
```
"I can't go on like this."
```

---

### Screenshot / Video
Attach a screenshot or short clip showing the issue.  
**For truncation/overflow:** always include a screenshot.  
**For subtitle sync:** always include a video clip.

---

### Additional Notes
```
This line appears in 3 other places in the game — searching for other instances recommended.
```

---

## 📝 Writing Tips

- **Be specific** — "spelling error" is not a title. Name the exact word and the fix.
- **One bug, one report** — don't bundle multiple issues in the same report.
- **Always include source text** — helps the translator fix it correctly.
- **Screenshot is worth a thousand words** — always capture the exact screen state.
- **Suggest the fix** when you know it — saves time for the translator.
- **Context counts** — if it's a context issue, describe what's happening in the game at that moment.

---

## 🚫 Common Mistakes to Avoid

| Mistake | Why it's a problem |
|---|---|
| Vague title like "Translation error in menu" | Impossible to locate without reproducing the whole game |
| Missing "expected text" | Translator doesn't know how to fix it |
| Not including source text | Fix might introduce new errors without the reference |
| Logging style preferences as bugs | Unless the style guide says otherwise, it's not a bug |
| Marking every synonym choice as "wrong" | Check the glossary first |
