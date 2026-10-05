# Common Localization Errors in Portuguese Games

> A practical reference of the most frequent bugs found in PT-BR and PT-PT game localizations.
> Study these patterns — they're what you'll be hunting for daily.

---

## 🔴 Category 1 — Literal / Machine Translation Artifacts

These are the errors most commonly introduced when translation quality is poor
or when machine translation (MT) is used without proper post-editing.

| English Source | Wrong PT-BR | Correct PT-BR | Why it's wrong |
|---|---|---|---|
| "You have 3 lives left" | "Você tem 3 vidas à esquerda" | "Você tem 3 vidas restantes" | "left" ≠ "left (direction)" |
| "Press A to attack" | "Pressione A para atacar" | "Pressione A para atacar" ✅ | Actually fine! |
| "Save your game" | "Salve seu jogo" | "Salve seu jogo" ✅ | Fine in BR context |
| "Load game" | "Carregar jogo" → "Carga do jogo" | "Carregar jogo" | Nominalizing unnecessarily |
| "It's a trap!" | "É uma armadilha!" | "É uma armadilha!" ✅ | Fine |
| "Game Over" | "Fim do Jogo" | Usually kept as "Game Over" | Depends on style guide — check |
| "Skip cutscene" | "Pular cena cortada" | "Pular cinemática" | "cutscene" ≠ "cena cortada" |

---

## 🟠 Category 2 — Glossary Violations (Most Common in LQA)

Terms that have approved translations but are translated differently:

| Term | Wrong | Correct (typical) | Note |
|---|---|---|---|
| Quest | Missão, Tarefa, Busca | Depends on glossary | Check project glossary |
| Skill | Habilidade, Perícia, Talento | Depends on glossary | Inconsistency is the bug |
| Level Up | Subiu de nível, Evoluiu | Depends on glossary | Must be consistent |
| Save Point | Ponto de salvamento, Checkpoint | Depends on glossary | |
| Health / HP | Vida, Saúde, HP | Depends on game genre | Action games often keep "HP" |
| Inventory | Inventário | Inventário ✅ | Usually consistent |
| Respawn | Renascer, Ressurgir, Reaparecer | Depends on glossary | |

---

## 🟡 Category 3 — Context Errors

Translations correct in isolation, wrong in game context:

### Gender agreement based on player character
```
Source: "You are the chosen one."
Wrong:  "Você é o escolhido."  (always masculine)
Right:  Depends on selected character gender — if female: "Você é a escolhida."
```
> ⚠️ If the game has character creation with gender selection, gender-neutral or
> gender-adaptive strings are critical to check.

### Register mismatch
```
Source: "Die, villain!"
Wrong:  "Faleça, vilão!" (extremely formal, literary — doesn't match an action game)
Right:  "Morra, vilão!" or "Morra, seu maldito!"
```

### Tense mismatch
```
Source: "The castle was destroyed."  (past narrative)
Wrong:  "O castelo é destruído."  (present — sounds like it's happening now)
Right:  "O castelo foi destruído."
```

---

## 🔵 Category 4 — Technical Errors

### Truncation
Text boxes in games have fixed pixel width. Longer languages = truncation risk.
```
English: "Continue"     (8 chars)
PT-BR:   "Continuar"    (9 chars) — usually fine
         "Prosseguir"   (10 chars) — may truncate in small buttons
```
> Always check: buttons, tooltips, item names, NPC speech bubbles.

### Missing Characters / Font Issues
Portuguese uses: `ã à á â ç é ê í ó ô õ ú ü`  
If the font doesn't support these, you'll see: `□`, `?`, or the base letter without accent.

```
Wrong render: "Esta e uma opcao" (all diacritics missing)
Right:        "Esta é uma opção"
```

---

## 🟣 Category 5 — Subtitle Sync Issues

| Issue | What it looks like |
|---|---|
| Early subtitle | Subtitle appears 0.5–2s before character speaks |
| Late subtitle | Subtitle appears after character finishes speaking |
| Duration too short | Subtitle disappears before player can read it |
| Duration too long | Subtitle lingers after audio ends |
| Wrong speaker | Subtitle attributed to wrong character |
| Orphaned subtitle | Subtitle appears when no audio is playing |

> For subtitle sync bugs: **video capture is mandatory**. Screenshots don't show timing.

---

## 📋 Top 10 Things to Always Check First

1. Main menu — fully translated?
2. Loading screens — any placeholder text?
3. First 5 minutes of gameplay — tutorial text, onboarding
4. Character creation screen — gender forms
5. Inventory/equipment screen — truncation prone
6. Settings/options menu — technical vocabulary
7. First major cutscene — subtitle sync, VO match
8. Error messages — often forgotten in localization
9. Achievement/trophy descriptions
10. End credits — translated team names (if required)
