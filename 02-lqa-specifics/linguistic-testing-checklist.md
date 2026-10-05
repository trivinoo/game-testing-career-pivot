# LQA Linguistic Testing Checklist

> Use this checklist when reviewing any section of a localized game.
> Adapt it with project-specific rules from the style guide.

---

## ✅ Section 1 — Spelling & Grammar

- [ ] No spelling mistakes
- [ ] Correct use of accents and diacritics (ã, ç, é, ê, ó, ô, etc.)
- [ ] Correct agreement: noun–adjective gender/number
- [ ] Correct verb conjugation and tense
- [ ] No missing or extra punctuation (periods, commas, question marks)
- [ ] Correct use of capital letters (sentence-initial, proper nouns, titles)
- [ ] No double spaces or trailing spaces

---

## ✅ Section 2 — Style & Tone

- [ ] Matches the register defined in the style guide (formal / informal / colloquial)
- [ ] Correct use of address form — **você** vs **tu** (BP) or **tu** vs **você/senhor** (EP)
- [ ] Character voice is consistent (a gruff warrior shouldn't suddenly sound polished)
- [ ] Genre tone is respected (horror ≠ comedy ≠ children's game)
- [ ] No literal/awkward translations that sound unnatural in Portuguese

---

## ✅ Section 3 — Consistency

- [ ] Same terms are translated the same way throughout (check glossary)
- [ ] Character names are consistent (if localized)
- [ ] Item/ability/spell names match the approved glossary
- [ ] Pronoun reference is consistent within dialogue sequences
- [ ] UI labels match in-game dialogue references (e.g., button name matches tutorial text)

---

## ✅ Section 4 — Context

- [ ] Translation makes sense given what's happening on screen
- [ ] Gender-ambiguous source strings are correctly resolved based on character shown
- [ ] Plural/singular is correct based on quantity shown in game
- [ ] Tense is appropriate (instructions: imperative / narrative: past / UI: present)
- [ ] Cultural references are appropriately adapted (if required by style guide)

---

## ✅ Section 5 — Technical / Display

- [ ] Text is not truncated (cut off at the edge of the UI box)
- [ ] Text does not overflow beyond the UI element bounds
- [ ] Special characters render correctly (no □ or ? replacement glyphs)
- [ ] Font supports all required characters for Portuguese (ã, ç, ê, etc.)
- [ ] No untranslated strings (source language visible in a localized build)
- [ ] No placeholder text visible (e.g., `[STRING_NOT_FOUND]`, `TODO`, `MISSING`)
- [ ] Correct line breaks — wrapping doesn't create awkward reading flow

---

## ✅ Section 6 — Subtitles & Audio

- [ ] Subtitle appears at the correct time (not too early, not too late)
- [ ] Subtitle duration is appropriate (enough time to read)
- [ ] Subtitle content matches the VO (not just the written script — the actual recording)
- [ ] Speaker attribution is correct (right character name shown)
- [ ] Subtitles present for all voiced lines in the localized build
- [ ] No subtitles appearing when there is no audio (orphaned subtitles)

---

## ✅ Section 7 — Metadata / Numbers / Symbols

- [ ] Decimal separators are correct (PT uses `,` not `.` for decimals)
- [ ] Thousands separators are correct (`.` in PT, or space in some contexts)
- [ ] Currency symbols if present are correct
- [ ] Date/time formats are adapted if required
- [ ] Units of measurement adapted if required (metric by default in PT/BR)

---

## 📝 Notes

- Always cross-reference with the **project glossary** before flagging a consistency issue
- Always check the **style guide** before flagging a style issue — it may be intentional
- When in doubt: log the bug as a **suggestion** or **minor** with a note asking for clarification
