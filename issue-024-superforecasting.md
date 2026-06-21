**Managing Machines · No. 024 · Daily**

*Leadership, systems & deep work — reread for the people who run the agents.*

*Today's Book*

# Superforecasting

![Cover of Superforecasting by Philip Tetlock & Dan Gardner](https://covers.openlibrary.org/b/isbn/9780804136716-L.jpg)

**by Philip Tetlock & Dan Gardner · 2015 · Decision Science**

> "Beliefs are hypotheses to be tested, not treasures to be guarded."

⏱ 8-min read · ★ 4.2 / 5 · 352 pages

**Read this if…** you make judgment calls under uncertainty — or run agents that do — and you want a measurable, trainable way to be *less wrong*. This is the engineer's manual for probability, not punditry.

---

## 01 — Key Takeaways

1. **Foxes beat hedgehogs.** Forecasters who know many small things, hold loosely-held views, and stitch together many perspectives ("foxes") reliably outpredict the confident single-Big-Idea "hedgehogs" the media loves.
2. **Keep score, or you're guessing.** Without numeric probabilities and tracked outcomes, no one can tell skill from luck. The Brier score makes accuracy auditable — and only then can it improve.
3. **Skill is trainable, not innate.** Superforecasters aren't geniuses or insiders. Their edge is method and mindset; a short training in probabilistic reasoning measurably improved ordinary volunteers.
4. **Break the question down (Fermi-ize).** Decompose an intimidating question into knowable and unknowable sub-parts. This "flushes ignorance into the open" instead of letting a gut feeling stand in for analysis.
5. **Start outside, then move inside.** Anchor on the base rate — how often things of this type happen — *before* adjusting for the specifics of this case. The outside view fights the vividness of the inside story.
6. **Update in small, frequent steps.** Treat each belief as a dial, not a switch. Nudge probabilities as evidence trickles in — neither over-reacting to noise nor clinging to a prior past its expiry.

---

## 02 — Core Concepts

**The Ten Commandments** — Tetlock's distilled, experimentally-supported playbook: triage; break problems down; balance outside and inside views; update on evidence; weigh clashing causal forces; granulate your probabilities; balance under- and over-confidence; learn from errors without blame or hindsight; team well; and treat the rules themselves as guidelines, not gospel.

**Fermi-izing** — decompose a hard question into estimable pieces (named for Enrico Fermi's back-of-envelope estimates). Make each assumption explicit and quantified, so the guesswork is visible and correctable.

**Outside View → Inside View** — get the base rate of the reference class first ("how often does this sort of thing happen?"), *then* adjust for case-specific detail. Doing it in that order curbs the storytelling bias of the inside view.

**Dragonfly Eye** — like a dragonfly's compound eye, synthesize many independent perspectives and sources into one aggregated view. Actively seek dissent; the synthesis beats any single lens.

**Calibration vs. Resolution (the Brier score)** — accuracy has two parts: calibration (when you say 70%, it happens ~70% of the time) and resolution (you make confident, decisive calls). The Brier score scores both against reality.

**Perpetual Beta** — the strongest predictor of becoming a superforecaster: a relentless commitment to belief-updating and self-improvement — roughly three times as predictive as raw intelligence. Treat your judgment like software that's never "done."

---

## 03 — The Book, Part by Part

**Ch. 1–3 — The case & the scorekeeping.** "An Optimistic Skeptic," "Illusions of Knowledge," and "Keeping Score" set the stakes: most expert prediction is no better than chance, but accuracy is real, measurable (Brier scores), and worth chasing.

**Ch. 4–7 — Who the superforecasters are.** "Superforecasters," "Supersmart?", "Superquants?", "Supernewsjunkies?" dismantle the easy explanations — it isn't IQ, math wizardry, or inside access. It's how they think.

**Ch. 8–9 — The mindset & the team.** "Perpetual Beta" reveals growth-mindset belief-updating as the top trait; "Superteams" shows how aggregating diverse, well-run groups beats lone forecasters.

**Ch. 10–12 — Leadership, doubts & the future.** "The Leader's Dilemma" reconciles decisive leadership with humble forecasting; "Are They Really So Super?" airs the honest caveats; "What's Next?" looks ahead. An appendix lists the Ten Commandments.

---

## 04 — Lines Worth Keeping

> "Beliefs are hypotheses to be tested, not treasures to be guarded."

> "The strongest predictor of rising into the ranks of superforecasters is perpetual beta, the degree to which one is committed to belief updating and self-improvement."

> "Forecasting is not a 'you have it or you don't' talent. It is a skill that can be cultivated."

---

## 05 — The Other Side · Opinions, Criticism & What to Read Next

**Why people love it:** The *Wall Street Journal* called it the most important book on decision making since *Thinking, Fast and Slow*. It's rare: a pop-science book built on a real, government-funded tournament (the Good Judgment Project) with hard scores, not anecdotes — and it turns "good judgment" from a mystique into a teachable checklist.

**Fair criticisms:** Knowing what superforecasting *is* isn't the same as knowing how to manufacture it — the training-to-impact link is thinner than the confident tone suggests. The whole edifice optimizes one metric (the Brier score) over short, resolvable, geopolitical questions; it says less about long-horizon, structurally novel, or one-shot events where base rates barely exist. Critics also wanted to see the raw distributions, and note that team-with-aggregation vs. prediction-market comparisons leave the "how robust is this?" question partly open. Tetlock, to his credit, is candid about much of this.

**Read next:** *Thinking, Fast and Slow* (Daniel Kahneman) for the bias machinery underneath; *Expert Political Judgment* (Tetlock's own earlier, more academic foxes-vs-hedgehogs study); and *Noise* (Kahneman, Sibony & Sunstein) for the variance side of bad judgment.

---

## ⚙ In the Agentic World Order

*How this book holds up when AI agents do the work.*

**Make agents keep score.** Tetlock's core demand — numeric probabilities, tracked against outcomes — is the missing discipline in most agent fleets. Have agents emit confidence levels, then Brier-score them. Only a calibrated agent can be *trusted* to act unsupervised; an uncalibrated one is a confident guesser.

**Fermi-ize the prompt; aggregate the dragonfly eye.** Decompose a hard task into estimable sub-questions an agent can actually answer, then run *many* independent agents and aggregate — the dragonfly eye becomes an ensemble. Diversity of approach beats one clever model, and the spread itself signals uncertainty.

**Outside view as a guardrail against confident hallucination.** Force the base-rate question — "how often does this kind of task succeed / this claim hold?" — before the agent commits to a vivid inside-view narrative. It's a structural check on plausible-sounding fabrication.

**Perpetual beta = the eval loop.** The top human trait — relentless belief-updating — is exactly the eval-and-retrain loop for a fleet. Treat prompts, tools, and policies as never "done": measure, update in small steps, and reward agents (and systems) that revise gracefully rather than commit hard and early.

---

### 🧠 This issue ships a skill

Install **Superforecasting** as a Claude Code skill — apply Philip Tetlock & Dan Gardner's frameworks to your work and your agent fleet on demand. Add the marketplace once, then install this book:

```
/plugin marketplace add hooperalex/managing-machines
/plugin install superforecasting
```

**[⤓ Browse the skill on GitHub →](https://github.com/hooperalex/managing-machines/tree/main/plugins/superforecasting)**

---

*Managing Machines — leadership, systems & deep work for the people who run the agents. [Browse the archive](https://simplebook.example/archive).*
