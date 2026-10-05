# Brazilian Portuguese vs. European Portuguese — Key Differences for LQA

> Understanding the differences between BP and EP is essential for LQA testing.
> Keywords Studios' job requires both — you must know which variant you're testing
> and apply the correct standards for each.

---

## 🌍 Overview

| | Brazilian Portuguese (PT-BR) | European Portuguese (PT-PT) |
|---|---|---|
| **Native speakers** | ~215 million | ~10 million |
| **Region** | Brazil | Portugal (+ Angola, Mozambique, etc.) |
| **Game market** | Large, growing rapidly | Smaller, often bundled with PT-BR |
| **Required by** | LATAM game releases | EU/European releases |

---

## 🔤 Linguistic Differences to Watch

### 1. Second Person Address (Critical for LQA)

| Context | PT-BR | PT-PT |
|---|---|---|
| Informal "you" | **você** (very common) | **tu** (most common in casual speech) |
| Formal "you" | **o senhor / a senhora** | **o senhor / a senhora** |
| Imperative (tu form) | Rarely used in informal BR | Common in PT: *"Vai lá!"* |
| Verb conjugation with "tu" | Often uses "você" form | Uses proper 2nd person: *"Tens"*, *"Vais"* |

> ⚠️ **LQA flag:** If a PT-BR text uses *"tu tens"* — that's a PT-PT contamination error.
> If a PT-PT text uses *"você"* in an informal context — check the style guide, it may be allowed.

---

### 2. Vocabulary Differences

| English | PT-BR | PT-PT |
|---|---|---|
| Bus | ônibus | autocarro |
| Train | trem | comboio |
| Cell phone | celular | telemóvel |
| Computer mouse | mouse | rato |
| Bathroom / Restroom | banheiro | casa de banho |
| Cool (slang) | legal | fixe |
| Car | carro | carro ✅ (same) |
| Apartment | apartamento | apartamento ✅ (same) |

> ⚠️ If a PT-BR game has "autocarro" — that's a localization error (wrong variant).

---

### 3. Spelling Differences (Post-Orthographic Agreement)

The 2009 Orthographic Agreement (Acordo Ortográfico) unified some spelling, but differences remain:

| English | PT-BR | PT-PT |
|---|---|---|
| Action | ação | ação ✅ (now unified) |
| Optimal | ótimo | ótimo ✅ (now unified) |
| Reception | recepção (old) / recepção | receção (PT preferred) |
| Direction | direção | direção ✅ |

> Note: Even after the agreement, many PT-PT speakers and publishers still use pre-agreement spelling.
> Always check which standard the project uses.

---

### 4. Gerund vs. Infinitive

| Context | PT-BR | PT-PT |
|---|---|---|
| "I'm going to eat" | Vou comer / Estou comendo | Vou comer / Estou a comer |
| Progressive form | *comendo* (gerund) | *a comer* (infinitive with "a") |

> ⚠️ "Estou comendo" in a PT-PT build = localization error (wrong variant).

---

### 5. Clitic Pronouns (Pronoun Placement)

| Context | PT-BR | PT-PT |
|---|---|---|
| "Give me" | Me dá / Dá pra mim | Dá-me |
| "He saw me" | Ele me viu | Ele viu-me |
| Proclisis (before verb) | Common | Used in specific grammatical contexts |
| Enclisis (after verb) | Less common in speech | Standard written form |

> ⚠️ *"Me dê"* in a PT-PT build may be flagged as a variant error — verify with style guide.

---

## 🎮 In-Game LQA Application

When you receive a PT-BR or PT-PT build:

1. **Confirm the target variant** — never assume
2. **Check the style guide** for variant-specific rules
3. **Flag wrong-variant vocabulary** (ônibus vs autocarro, etc.)
4. **Flag wrong-variant grammar** (gerund vs. a+infinitive, tu vs. você)
5. **Do NOT flag things correct in one variant if you're testing the other**

---

## 📚 Quick Reference Cards

### Common Flags in PT-BR Builds
- `tu tens / tu vais / tu és` → should be `você tem / você vai / você é`
- `a comer / a jogar` → should be `comendo / jogando`
- `autocarro / telemóvel / casa de banho` → wrong variant vocabulary

### Common Flags in PT-PT Builds
- `você` in informal dialogue → may need to be `tu` (check style guide)
- `comendo / jogando` → should be `a comer / a jogar`
- `ônibus / celular / banheiro` → wrong variant vocabulary
