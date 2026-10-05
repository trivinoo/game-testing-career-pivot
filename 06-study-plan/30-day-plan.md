# 30-Day LQA Study Plan

> Designed for someone with 3+ years of software QA experience.
> Focused on closing the **game-specific and localization-specific** knowledge gaps.
> Time commitment: ~1 hour/day.

---

## Week 1 — Orientation & Foundations

| Day | Topic | Resource |
|---|---|---|
| 1 | Read: Software QA → Game QA parallels | [`01-fundamentals/software-qa-vs-game-qa.md`](../01-fundamentals/software-qa-vs-game-qa.md) |
| 2 | Read: What is LQA? | [`02-lqa-specifics/what-is-lqa.md`](../02-lqa-specifics/what-is-lqa.md) |
| 3 | Read: Game testing types | [`01-fundamentals/game-testing-types.md`](../01-fundamentals/game-testing-types.md) |
| 4 | Study: LQA bug categories & severity | [`03-bug-reporting/bug-report-template.md`](../03-bug-reporting/bug-report-template.md) |
| 5 | Practice: Write 3 bug reports from any PT-BR game you own | Use the template |
| 6 | Review: Good vs Bad bug reports | [`03-bug-reporting/examples/`](../03-bug-reporting/examples/) |
| 7 | Rest / Review week 1 notes | — |

---

## Week 2 — LQA Deep Dive

| Day | Topic | Resource |
|---|---|---|
| 8 | Study: Linguistic testing checklist | [`02-lqa-specifics/linguistic-testing-checklist.md`](../02-lqa-specifics/linguistic-testing-checklist.md) |
| 9 | Study: BP vs EP differences | [`05-portuguese-lqa/bp-vs-ep-differences.md`](../05-portuguese-lqa/bp-vs-ep-differences.md) |
| 10 | Study: Common localization errors | [`05-portuguese-lqa/common-localization-errors.md`](../05-portuguese-lqa/common-localization-errors.md) |
| 11 | Practice: Play a game in PT-BR for 1 hour, apply the checklist | Any available PT-BR title |
| 12 | Practice: Find and document 5 real bugs in a PT-BR game | Use bug report template |
| 13 | Watch: Game localization process (YouTube — see resources below) | External |
| 14 | Rest / Review week 2 notes | — |

---

## Week 3 — Tools & Workflow

| Day | Topic | Resource |
|---|---|---|
| 15 | Study: Tools overview | [`04-tools/game-testing-tools.md`](../04-tools/game-testing-tools.md) |
| 16 | Practice: Set up OBS or ShareX for screen capture | External |
| 17 | Practice: Capture subtitle sync issue (look for one in a PT-BR game) | Real game |
| 18 | Study: Localization workflow (how LQA fits in the pipeline) | [`02-lqa-specifics/what-is-lqa.md`](../02-lqa-specifics/what-is-lqa.md) |
| 19 | Practice: Write 5 more bug reports — include one video attachment | — |
| 20 | Read: Keywords Studios careers page, LQA blog posts | External |
| 21 | Rest / Consolidate portfolio bugs | — |

---

## Week 4 — Portfolio & Interview Prep

| Day | Topic | Resource |
|---|---|---|
| 22 | Build portfolio: Polish 10 best bug reports | [`07-portfolio/`](../07-portfolio/) |
| 23 | Interview prep: Common LQA interview questions | See below |
| 24 | Interview prep: Map your software QA experience to game QA | [`01-fundamentals/software-qa-vs-game-qa.md`](../01-fundamentals/software-qa-vs-game-qa.md) |
| 25 | Apply: Update CV to highlight transferable skills | — |
| 26 | Apply: Write cover letter for Keywords Studios | — |
| 27 | Practice: Mock interview (record yourself answering questions) | See questions below |
| 28 | Final review: Walk through the full checklist in a game | — |
| 29 | Send application! | — |
| 30 | Celebrate + keep playing games in PT-BR 🎮 | — |

---

## 🎙️ Common LQA Interview Questions

Prepare answers for these (mapping your software QA experience):

1. **"What experience do you have with testing?"**  
   → Lead with your 3+ years of software QA. Explain the parallels. Show self-awareness of what's new.

2. **"What would you do if you found a bug but you weren't sure if it was intentional?"**  
   → Log it as a query/suggestion. Explain your reasoning. Ask for clarification from the LQA lead.

3. **"How would you handle a string that's grammatically correct but sounds unnatural?"**  
   → Flag it as a linguistic quality issue / suggestion. Include the source text and a suggested improvement.

4. **"You're testing Chapter 3 and you find the same error in 20 different lines. How do you handle it?"**  
   → Log one representative bug, note it's a systemic issue, search for all instances, and attach a list.

5. **"What's the difference between PT-BR and PT-PT?"**  
   → Know your gerund/a+infinitive, você/tu, vocabulary differences. See the reference doc.

6. **"Have you played many video games?"**  
   → Be honest. If yes, mention genres and platforms. If no, mention you're actively playing more now.

7. **"Describe your process for testing a new build."**  
   → Read build notes → Identify new content → Run assigned test areas → Check regression list → Report bugs.

---

## 📚 External Resources

### YouTube
- Search: "Game Localization QA" — many GDC talks available free
- Search: "How games are localized" — great for pipeline understanding
- [Localization Lab channel](https://www.youtube.com/@localizationlab) — if available

### Reading
- [IGDA Localization SIG resources](https://localization.igda.org/)
- [Gamasutra/GameDeveloper.com — localization articles](https://www.gamedeveloper.com/)
- [Slator — games localization news](https://slator.com/tag/games/)
- Keywords Studios blog: [https://www.keywordsstudios.com/blog](https://www.keywordsstudios.com/blog)

### Practice Games (PT-BR available, good for finding bugs)
- **The Sims 4** (EA — free to play, lots of text, known localization quirks)
- **League of Legends** (Riot — vast amount of text, good PT-BR coverage)
- **Assassin's Creed** series (Ubisoft — cinematic, subtitles, VO)
- **Final Fantasy XIV** (Square Enix — large PT-BR community, rich text)
- **Cyberpunk 2077** (CD Projekt Red — excellent PT-BR localization to learn from)
