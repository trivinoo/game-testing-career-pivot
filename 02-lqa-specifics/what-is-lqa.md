# What Is LQA? — Localization Quality Assurance Explained

---

## 🌍 Definition

**Localization QA (LQA)** is the process of testing a localized (translated) product —
in this case, a video game — to verify that the translated content is:

1. **Linguistically correct** — proper grammar, spelling, punctuation
2. **Contextually appropriate** — makes sense given what's happening in the game
3. **Consistent** — follows the approved glossary and style guide
4. **Technically integrated** — text renders correctly on screen (no truncation, font issues, etc.)
5. **In sync** — subtitles match audio, text matches VO timing

> LQA testers are **the last line of defense** before players see the translated content.

---

## 🔍 LQA vs. Translation — What's the Difference?

| | Translator | LQA Tester |
|---|---|---|
| **Works with** | Source text in a CAT tool | Translated text *in the game itself* |
| **Context** | Reads strings in isolation | Sees strings as the player sees them |
| **Goal** | Produce the translation | Verify the translation is correct in context |
| **Catches** | Linguistic errors during translation | Linguistic + technical errors after integration |

**Critical insight:** A translation can be correct in isolation but wrong in context.

> 📌 Example: A string that says *"Key"* in English might be translated as *"Chave"* (physical key),
> but if it refers to a keyboard key, the correct translation is *"Tecla"*.
> The translator working in a spreadsheet might not know — the LQA tester playing the game will.

---

## 🧪 What Does an LQA Tester Do Day-to-Day?

### Typical daily workflow:
1. **Receive build notes** — what changed in the new build
2. **Load the game** on PC or console
3. **Navigate to assigned sections** — specific chapters, menus, cutscenes
4. **Compare on-screen text** against source (English) using a reference document
5. **Check each string** for linguistic quality and technical correctness
6. **Write bug reports** for every issue found
7. **Retest previously reported bugs** that are marked as fixed (regression)
8. **Update tracking spreadsheet / bug tracker** with status

### Tools used daily:
- Bug tracker (JIRA, DevTrack, or internal)
- Reference spreadsheet (translation memory export)
- Style guide (PDF/wiki)
- Glossary (approved term list)
- The game itself (on devkit or PC client)

---

## 📋 LQA Bug Categories

| Category | Description |
|---|---|
| **Linguistic** | Grammar, spelling, punctuation errors |
| **Consistency** | Inconsistent translation of the same term |
| **Context** | Correct translation but wrong for the game context |
| **Truncation** | Text cut off — doesn't fit the UI box |
| **Subtitle sync** | Subtitle appears before/after/without matching audio |
| **Missing string** | Text not translated, shows in source language or blank |
| **Overflow** | Text overflows outside UI element |
| **Font/Encoding** | Special characters (ã, ç, é) not rendering |
| **Hardcoded** | Text that should be translated but is baked into code |
| **Style guide violation** | Breaks agreed rules (e.g., formal vs informal address) |
| **Glossary violation** | Uses unapproved translation for a key term |

---

## 🎯 The Immersion Standard

The Keywords Studios job ad says:
> *"Your choice of words will directly influence the extent of players' immersion in the virtual world."*

This is the core philosophy of LQA. The test isn't just "is this grammatically correct?" —
it's **"does this feel like it belongs in this game world?"**

Ask yourself:
- Does the tone match the character speaking?
- Does the formality level match the genre (RPG, action, comedy)?
- Would a native speaker find this natural or awkward?
- Does this match how the term was used earlier in the game?
