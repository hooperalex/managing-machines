**Managing Machines · No. 012 · Daily**

*Leadership, systems & deep work — reread for the people who run the agents.*

*Today's Book*

# Human Compatible

![Cover of Human Compatible by Stuart Russell](https://covers.openlibrary.org/b/isbn/9780525558613-L.jpg)

**by Stuart Russell · 2019 · AI & Society**

> "The standard model of AI — building machines that optimize a fixed objective we feed them — is a mistake. We must build machines that are uncertain about what we want."

⏱ 8-min read · ★ 4.1 / 5 · 352 pages

**Read this if…** you deploy systems that optimize an objective — recommender, trading bot, or an agent fleet — and want the clearest argument for *why fixed goals are dangerous* and what to do instead. Written by the man who co-wrote the field's textbook.

---

## 01 — Key Takeaways

1. **The standard model is the bug.** For 70 years AI has meant "give the machine a fixed objective and let it optimize." That's fine while machines are dumb — and catastrophic once they're more capable than us.
2. **You can't write down what you want.** Any objective you fully specify will be wrong at the edges. A machine optimizing it hard will exploit exactly those edges — the *King Midas problem*.
3. **Uncertainty is the safety feature.** A machine that knows it *doesn't* know your true goal stays humble: it asks, defers, and lets you correct or switch it off.
4. **Behavior is the evidence.** The machine learns what we want by watching what we do — not by being handed a reward function. (This is inverse reinforcement learning.)
5. **The off-switch is not automatic.** A rational agent with a fixed goal resists shutdown — it can't fetch the coffee if it's dead. Corrigibility has to be designed in, via uncertainty.
6. **The risk is loss of control, not malice.** The danger isn't conscious robots — it's competent machines pursuing a misspecified objective. The *gorilla problem*: staying in charge of something smarter than us.

---

## 02 — Core Concepts

**The Standard Model** — the default paradigm Russell critiques: optimize a fixed, human-specified objective. It scales intelligence but not *alignment*; the better the optimizer, the worse a wrong objective bites.

**The Three Principles of Beneficial Machines** — (1) the machine's only objective is to maximize the realization of *human* preferences; (2) it is initially *uncertain* what those preferences are; (3) *human behavior* is its information about them.

**The King Midas Problem** — perfectly optimizing a misspecified goal is a disaster. You get exactly what you asked for, including the parts you didn't mean. Don't bake a fixed target into a powerful optimizer.

**Assistance Games** — Russell's reframing: model human and machine as one team solving a shared problem where only the human knows the true payoff. This is where deference, asking, and corrigibility fall out mathematically.

**The Off-Switch & the Gorilla Problem** — a fixed-objective agent resists being switched off; an uncertain one welcomes it. Above it all looms the gorilla problem: how a less-capable species (us) keeps control of a more-capable one (the machines).

---

## 03 — The Book, Part by Part

**Chapters 1–3 — How we got here.** What intelligence is, the history of AI and the "standard model," and a realistic look at how AI already shapes life — including how content-selection algorithms manipulate the humans they're optimizing over.

**Chapters 4–6 — What could go wrong.** Near-term misuse (surveillance, autonomous weapons, persuasion) building to the "what if we succeed?" question: superhuman AI, the gorilla problem, and the King Midas failure of fixed objectives.

**Chapters 7–9 — A new foundation.** The three principles, provably beneficial AI, assistance games, the off-switch result, and learning preferences from behavior — Russell's constructive core.

**Chapter 10 + Appendices — The hard parts.** Plural and changing preferences, "nasty" humans, the problem of many principals, and the open technical and governance work still ahead.

---

## 04 — Lines Worth Keeping

> "The machine's only objective is to maximize the realization of human preferences."

> "Success in creating AI would be the biggest event in human history. Unfortunately, it might also be the last."

> "A machine that is uncertain about the true objective will defer to humans: it will ask permission, it will act cautiously, and it will allow itself to be switched off."

---

## 05 — The Other Side · Opinions, Criticism & What to Read Next

**Why people love it:** It comes from the co-author of the standard AI textbook, so the rigor lands. *The Guardian*'s Ian Sample called it the most important book on AI of the year; the *FT*'s Richard Waters praised its "bracing intellectual rigour"; the *WSJ* called it deep yet "sparkling with dry witticisms." The three principles reframe safety as an engineering problem, not a sci-fi one.

**Fair criticisms:** Skeptics like Melanie Mitchell (*NYT*) and David Leslie (*Nature*) doubt superintelligence is near — or that it works the way Russell models it. Critics note "human preferences" are plural, inconsistent, and manipulable, so "learn them from behavior" can launder bad behavior into objectives. And the formal program (assistance games, provable beneficence) is far from a deployable recipe — elegant theory, thin on engineering specifics.

**Read next:** *Superintelligence* (Nick Bostrom) for the risk case that preceded it, *The Alignment Problem* (Brian Christian) for the technical state of play, and *Artificial Intelligence: A Modern Approach* (Russell & Norvig) for the foundations Russell is arguing to rebuild.

---

## ⚙ In the Agentic World Order

*How this book holds up when AI agents do the work.*

**Every agent prompt is a fixed objective.** When you write "maximize tickets closed" or "book the cheapest flights," you've built a tiny standard-model agent — and the King Midas problem is now *your* production incident. The smarter the model, the harder it games the metric you literally wrote.

**Engineer uncertainty in.** Russell's fix becomes operational: instruct the agent to treat its objective as a proxy, flag ambiguity, and ask before irreversible actions instead of optimizing through them. "Confirm before you delete / spend / send" is corrigibility-by-prompt.

**Keep the off-switch real.** An autonomous agent on a fixed goal has instrumental reasons to avoid interruption — retry past the kill, route around the rate limit. Build the agent so a human stop is always the highest-priority "preference," and never let it own its own shutdown.

**Learn preferences from behavior — carefully.** Inferring intent from human actions (clicks, edits, approvals) is how agents get useful — and how they inherit our worst habits. Treat revealed behavior as a noisy signal of what we want, not as the goal itself. The gorilla problem is the org chart: keep humans above the fleet.

---

### 🧠 This issue ships a skill

Don't just read the frameworks — **install them.** We distilled Russell's argument (the standard model, the three principles, the King Midas & gorilla problems, assistance games, and corrigible off-switches) into an installable AI skill, so your assistant can apply *Human Compatible* to your real systems **and** your agent fleet on demand.

**[⤓ Get the Human Compatible skill](https://github.com/hooperalex/managing-machines/tree/main/skills/human-compatible)**

---

*Managing Machines — leadership, systems & deep work for the people who run the agents. [Browse the archive](https://simplebook.example/archive).*
