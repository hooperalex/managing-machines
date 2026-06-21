**Managing Machines · No. 028 · Daily**

*Leadership, systems & deep work — reread for the people who run the agents.*

*Today's Book*

# The Design of Everyday Things

![Cover of The Design of Everyday Things by Don Norman](https://covers.openlibrary.org/b/isbn/9780465050659-L.jpg)

**by Don Norman · 1988 / 2013 · Design & Psychology**

> "When you have trouble with things — whether it's figuring out whether to push or pull a door — it's not your fault. Don't blame yourself: blame the designer."

⏱ 8-min read · ★ 4.2 / 5 · 368 pages

**Read this if…** you build interfaces a human — or an agent — has to operate without a manual, and you want a precise vocabulary for *why* things confuse people. This is the foundational text of human-centered design.

---

## 01 — Key Takeaways

1. **It's not your fault — it's the design.** When something is hard to use, the system is badly designed, not the human stupid. Norman renames "human error" as *system error*.
2. **Discoverability and understanding** are the two most important properties of good design: can you figure out what actions are possible, and can you tell what's going on?
3. **Affordances tell you what's possible; signifiers tell you where.** A flat plate *affords* pushing; the visible plate is the *signifier* that says "push here." Hide the signifier and you get the "Norman door."
4. **People run on a conceptual model.** Users act on the mental story they've built — right or wrong. Your job is to make the system's model match the one in their head.
5. **Close the two gulfs.** The *gulf of execution* (can I do what I intend?) and the *gulf of evaluation* (can I tell what happened?) are bridged by good mapping, constraints, and feedback.
6. **Design for error, because error is normal.** Distinguish *slips* (right plan, wrong execution) from *mistakes* (wrong plan). Add constraints, confirmations, and undo so the inevitable error is survivable.

---

## 02 — Core Concepts

**The Six Fundamental Principles** — affordances, signifiers, constraints, mapping, feedback, and a conceptual model. The whole toolkit for making a thing usable without instructions.

**Affordances & Signifiers** — affordances are the possible actions between object and user; signifiers are the perceptible signals that reveal them. Good design makes the right action *obvious*.

**The Seven Stages of Action** — goal → plan → specify → perform → perceive → interpret → compare. A cycle for diagnosing exactly *where* an interaction breaks down.

**The Two Gulfs** — the gulf of *execution* (turning intent into action) and the gulf of *evaluation* (reading the system's state). Good design narrows both.

**Human-Centered Design & Error** — design for people as they are, not as you wish them to be. Treat slips and mistakes as design problems to engineer around, not user failings to scold.

---

## 03 — The Book, Part by Part

**Ch. 1 — The Psychopathology of Everyday Things.** The famous "Norman doors" open the case: the six principles, and why bad design — not bad users — causes most trouble.

**Ch. 2 — The Psychology of Everyday Actions.** The seven stages of action, the two gulfs, and how people assign blame (usually to themselves, wrongly).

**Ch. 3 — Knowledge in the Head and in the World.** Why we offload memory onto the environment, and how constraints and good mapping let the world do the remembering.

**Ch. 4 & 5 — Knowing What to Do; Human Error.** Constraints, conventions, and forcing functions; the taxonomy of slips vs. mistakes and how to design so errors don't become disasters.

**Ch. 6 & 7 — Design Thinking; Design in the World of Business.** The double-diamond process, solving the right problem, and the messy reality where feature creep and incentives fight good design.

---

## 04 — Lines Worth Keeping

> "Two of the most important characteristics of good design are discoverability and understanding."

> "Good design is actually a lot harder to notice than poor design, in part because good designs fit our needs so well that the design is invisible."

> "Affordances define what actions are possible. Signifiers specify how people discover those possibilities."

---

## 05 — The Other Side · Opinions, Criticism & What to Read Next

**Why people love it:** it's the founding text of HCI and UX — the book that gave a generation a shared vocabulary (affordance, signifier, mapping, feedback) for talking about why things work or don't. Once you read it you cannot un-see the bad doors, stoves, and dialog boxes everywhere.

**Fair criticisms:** it's repetitive and example-heavy — the core ideas could fit in a long essay, and the same door/stove anecdotes recur. The terminology has drifted: Norman himself muddied "affordance" so badly he had to bolt on "signifier" in 2013. It diagnoses bad design brilliantly but is thin on the *incentive* question it raises — when business pressures and feature creep cause bad design, the book names the problem then drifts back to ranting about it rather than solving it. And its everyday-object lens undersells the harder problems of complex, networked, software-first systems.

**Read next:** *The Inmates Are Running the Asylum* (Alan Cooper) for software-specific interaction design, *Don't Make Me Think* (Steve Krug) for the fast practical version, and Norman's own *Emotional Design* for the part this book underweights — how feeling, not just function, drives use.

---

## ⚙ In the Agentic World Order

*How this book holds up when your "user" is an AI agent.*

**Tools are affordances; their descriptions are signifiers.** An agent can only do what its tools afford — and it only *discovers* those actions through the tool name, schema, and docstring. A vague description is a hidden signifier: the Norman door of the agent world. Make the right call obvious.

**The system prompt is the conceptual model.** The agent acts on the mental model you hand it. When behavior is wrong, the model in the prompt and the model the task needs have diverged — fix the model, not the symptom.

**Close the two gulfs with tool ergonomics and feedback.** Gulf of execution: can the agent express its intent in the tools you gave it? Gulf of evaluation: does the tool return state legible enough for the agent to know what happened? Terse or ambiguous tool output is an evaluation gulf that produces loops and hallucinated success.

**Design for error — it's not the agent's fault.** Slips and mistakes are normal; "the agent is dumb" is usually system error. Add constraints (typed args, allow-lists), forcing functions (confirmations on destructive calls), and undo (dry-runs, reversible writes) so an inevitable bad call is survivable, not catastrophic.

---

### 🧠 This issue ships a skill

Install **The Design of Everyday Things** as a Claude Code skill — apply Don Norman's frameworks to your work and your agent fleet on demand. Add the marketplace once, then install this book:

```
/plugin marketplace add hooperalex/managing-machines
/plugin install the-design-of-everyday-things
```

**[⤓ Browse the skill on GitHub →](https://github.com/hooperalex/managing-machines/tree/main/plugins/the-design-of-everyday-things)**

---

*Managing Machines — leadership, systems & deep work for the people who run the agents. [Browse the archive](https://simplebook.example/archive).*
