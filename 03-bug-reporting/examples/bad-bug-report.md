# LQA Bug Report — Bad Example (and Why It Fails)

**Language:** PT-BR  
**Bug ID:** LQA-0099

---

## Title
`Translation error`

## Steps to Reproduce
1. Play the game
2. There's a mistake

## Current Text
bad translation

## Expected Text
should be better

---

> ❌ **Why this is a bad bug report:**

| Problem | Impact |
|---|---|
| Title is useless — "translation error" describes 90% of all LQA bugs | Developer/PM can't triage without reproducing the whole game |
| No location/path | Nobody can find the bug without guessing |
| No source text | Translator doesn't know what the original said |
| No screenshot | For visual bugs (truncation, overflow) this is critical |
| "bad translation" and "should be better" are not actionable | What exactly is wrong? What should it say? |
| No severity | Can't be prioritized in the backlog |
| No specific steps | Not reproducible by another tester or developer |

---

## The Same Bug Done Right

**Title:** `[PT-BR][CONTEXT] "Chave" should be "Tecla" — inventory tutorial references wrong key type`

**Steps to Reproduce:**
1. Start New Game
2. Reach the inventory tutorial (automatically triggered after first combat)
3. Read the tutorial prompt that appears in the top-right corner

**Location:** `New Game → First Combat → Inventory Tutorial → Tooltip Line 1`

**Current Text:** `"Pressione a chave para abrir o inventário."`

**Expected Text:** `"Pressione a tecla para abrir o inventário."`

**Source Text:** `"Press the key to open your inventory."`

**Severity:** Major — Refers to a physical key (door/lock) instead of a keyboard key, confusing the player.

**Screenshot:** [attached]

**Notes:** "Chave" = physical key; "Tecla" = keyboard/button key. Likely a context-blind translation. Glossary entry for "Key [keyboard]" = "Tecla" — this is a glossary violation.
