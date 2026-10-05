# LQA Bug Report — Good Example

**Language:** Brazilian Portuguese (PT-BR)  
**Bug ID:** LQA-0042  
**Status:** Open  
**Reported by:** QA Tester  
**Build:** v0.9.12

---

## Title
`[PT-BR][SPELLING] Verb conjugation error in Chapter 2 interrogation scene — "posse" should be "posso"`

## Category
Linguistic — Spelling / Conjugation

## Severity
**Major** — Incorrect verb form visible during a key emotional story moment.

## Language
Brazilian Portuguese (PT-BR)

## Steps to Reproduce
1. Launch the game from the main menu
2. Load Chapter 2: "A Verdade" (save file or chapter select)
3. Progress through the interrogation sequence until the protagonist speaks
4. Observe the subtitle on the protagonist's third line of dialogue

## Location / Path
```
Chapter 2: A Verdade → Interrogation Scene → Protagonist Dialogue → Line 3
```

## Current Text (What you see in-game)
> *"Eu não posse continuar assim."*

## Expected Text
> *"Eu não posso continuar assim."*

## Source Text (English reference)
> *"I can't go on like this."*

## Screenshot
![screenshot showing subtitle error](./assets/lqa-0042-screenshot.png)

## Additional Notes
- "posse" is a noun ("possession"/"posse") — completely different word, changes the meaning
- Searched remaining dialogue: this conjugation error appears only in this instance
- Suggested fix confirmed correct by checking against PT-BR grammar reference

---

> ✅ **Why this is a good bug report:**
> - Specific title with exact wrong/right words
> - Includes source text for reference
> - Single clear issue
> - Precise location path
> - Explains *why* it's wrong (not just "it's wrong")
> - Notes that other instances were checked (saves regression time)
