# Portfolio — Sample Mock Bug Reports

> These are practice bug reports you can build and refine to show employers.
> When applying to Keywords Studios or similar roles, a portfolio of 5–10 solid
> bug reports is a strong differentiator.

---

## How to Build Your Portfolio

1. **Play any game available in PT-BR or PT-PT** (even free-to-play)
2. **Switch the game language to Portuguese**
3. **Apply the LQA checklist** from [`02-lqa-specifics/linguistic-testing-checklist.md`](../02-lqa-specifics/linguistic-testing-checklist.md)
4. **Document every real issue you find** using the bug report template
5. **Polish 5–10 of your best reports** to include in your portfolio

---

## Mock Bug Report #1 — Spelling Error

**Bug ID:** PORTFOLIO-001  
**Game:** [Any RPG] (practice mock)  
**Language:** PT-BR  
**Build:** Retail / Latest patch  
**Date Found:** [Date]

### Title
`[PT-BR][SPELLING] "posso" misspelled as "posse" — protagonist dialogue, Act 1 opening`

### Category
Linguistic — Spelling

### Severity
Major

### Steps to Reproduce
1. Launch the game
2. Start a New Game
3. Wait for the opening cutscene to complete (approx. 3 minutes)
4. Observe the protagonist's first voiced line — read the subtitle

### Location
`Main Menu → New Game → Opening Cutscene → Protagonist Line 1`

### Current Text
> *"Eu não posse fazer isso."*

### Expected Text
> *"Eu não posso fazer isso."*

### Source Text
> *"I can't do this."*

### Severity Justification
"Posse" is an entirely different word (possession/posse), completely changing the meaning of the sentence. This appears in the first cutscene, making it a high-visibility error.

### Screenshot
[Attach screenshot]

---

## Mock Bug Report #2 — Truncation

**Bug ID:** PORTFOLIO-002  
**Language:** PT-BR

### Title
`[PT-BR][TRUNCATION] "Inventário" truncated to "Inventár..." in pause menu tab`

### Category
Truncation

### Severity
Major

### Steps to Reproduce
1. Start any game session
2. Press ESC / Start to open the pause menu
3. Navigate to the third tab (Inventory)
4. Observe the tab label text

### Location
`In-Game → Pause Menu → Inventory Tab → Tab Label`

### Current Text (on screen)
> *"Inventár..."*

### Expected Text
> *"Inventário"*

### Source Text
> *"Inventory"*

### Notes
The Portuguese word is 2 characters longer than the English. UI box not sized for Portuguese text.  
Possible fixes: reduce font size, widen tab, use abbreviation per style guide (e.g. "Inv.").

### Screenshot
[Attach screenshot showing the truncation clearly]

---

## Mock Bug Report #3 — Wrong Variant

**Bug ID:** PORTFOLIO-003  
**Language:** PT-BR

### Title
`[PT-BR][WRONG VARIANT] "Autocarro" used instead of "Ônibus" — PT-PT vocabulary in PT-BR build`

### Category
Localization — Wrong Variant

### Severity
Major

### Steps to Reproduce
1. Start a New Game
2. Reach the city hub area (Chapter 2)
3. Interact with the fast travel terminal
4. Read the transport option text in the menu

### Location
`Chapter 2: City Hub → Fast Travel Terminal → Transport Options → Option 2`

### Current Text
> *"Apanhe o autocarro para o aeroporto."*

### Expected Text
> *"Pegue o ônibus para o aeroporto."*

### Source Text
> *"Take the bus to the airport."*

### Notes
"Autocarro" is the PT-PT word for bus. In Brazil, "ônibus" is standard. This suggests the PT-PT translation was accidentally used in the PT-BR build, or the translator used the wrong variant.  
Also note: "Apanhe" (PT-PT imperative) should be "Pegue" in PT-BR.

---

## Mock Bug Report #4 — Subtitle Sync

**Bug ID:** PORTFOLIO-004  
**Language:** PT-BR

### Title
`[PT-BR][SUBTITLE SYNC] Subtitle appears ~1.5 seconds before VO begins — Chapter 3 NPC conversation`

### Category
Subtitle Sync — Early Subtitle

### Severity
Major

### Steps to Reproduce
1. Load Chapter 3: "O Refúgio"
2. Approach the innkeeper NPC near the entrance
3. Trigger dialogue (press E / Square / X)
4. Observe the first subtitle line vs. when the audio actually starts

### Location
`Chapter 3: O Refúgio → Innkeeper NPC → Dialogue Line 1`

### Expected Behavior
Subtitle should appear at the same time as (or 0.1–0.2s after) the start of the VO line.

### Actual Behavior
Subtitle appears approximately 1.5 seconds before the VO begins, breaking immersion and revealing the line before it is spoken.

### Video
[Attach video clip — mandatory for sync bugs]

### Notes
Only the first line of this dialogue has this issue. Remaining lines appear correctly synced.

---

## 💡 Tips for Your Portfolio

- **Use real games** — it's more credible than fully made-up scenarios
- **Include screenshots and video** — they demonstrate attention to detail
- **Vary your bug types** — show you can find Linguistic, Truncation, Context, and Sync issues
- **Add a brief intro page** explaining your background and why you're pivoting to LQA
- **Format consistently** — same fields, same structure, every report
- Host on **GitHub** or present as a **PDF document** depending on how you apply
