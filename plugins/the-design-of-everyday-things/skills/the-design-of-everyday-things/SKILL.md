---
name: the-design-of-everyday-things
description: Apply Don Norman's The Design of Everyday Things frameworks — the six fundamental principles (affordances, signifiers, constraints, mapping, feedback, conceptual model), discoverability vs understanding, the seven stages of action, the gulf of execution and gulf of evaluation, human-centered design, and design-for-error (slips vs mistakes, forcing functions). Use when the user is designing or critiquing an interface, API, tool, form, or workflow that someone must operate without a manual; diagnosing why something is confusing or error-prone; or doing the equivalent while designing the tools and prompts that an AI agent fleet must operate.
---

# The Design of Everyday Things — Don Norman's frameworks, as a skill

Source: *The Design of Everyday Things* (Don Norman, 1988; revised 2013). This skill lets you
**apply** Norman's design toolkit, not just describe it. Extracted by Managing Machines, Issue 028.

## When to use
- The user is designing or reviewing a UI, API, CLI, form, tool surface, or workflow.
- Something is confusing, error-prone, or generates support tickets — and you need to find *why*.
- A delegation question: how do I make the right action obvious without a manual?
- Designing the tools, schemas, and system prompts an AI agent must operate.
- Deciding how to make an inevitable error survivable rather than catastrophic.

## Core principle
**When a thing is hard to use, the thing is badly designed — not the person stupid.** Most
"human error" is *system error*. Design for people (and agents) the way they actually are, not
the way you wish they were. The two properties that matter most: **discoverability** (can you
figure out what's possible?) and **understanding** (can you tell what's going on?).

## The frameworks

**The Six Fundamental Principles** — the toolkit for usable-without-instructions design.
*Procedure:* check each: (1) **affordances** — what actions are possible? (2) **signifiers** —
what perceptible signal reveals them? (3) **constraints** — what stops wrong actions? (4)
**mapping** — do controls map naturally to effects? (5) **feedback** — is every action
acknowledged? (6) **conceptual model** — does the design tell a coherent story? *Use when*
auditing or building any interface.

**Affordances vs Signifiers** — affordances are possible actions; signifiers are the perceptible
cues that advertise them. *Procedure:* list the actions the design *affords*; for each, point to
the concrete signifier that reveals it (label, shape, icon, schema field); any affordance with no
signifier is invisible — add one or remove the affordance. *Use when* "they didn't know they
could do X" or a control exists but nobody finds it.

**The Seven Stages of Action** — one goal, then three *execution* stages (plan the action,
specify the action sequence, perform it) and three *evaluation* stages (perceive the world's
state, interpret it, compare it to the goal). *Procedure:* take a real task and walk it through
all seven stages in order; the first stage a person/agent can't complete is the defect. *Use
when* you need to locate *exactly where* an interaction fails, not just that it does.

**The Two Gulfs** — the gulf of **execution** (turning intent into action) and the gulf of
**evaluation** (reading the system's resulting state). *Procedure:* ask "can they easily do what
they intend?" (execution) and "can they easily tell what happened?" (evaluation); narrow the
wider gulf first with mapping/constraints (execution) or feedback (evaluation). *Use when*
people act but can't tell if it worked, or can't figure out how to act at all.

**Human-Centered Design** — start from real human needs and observed behavior, iterate.
*Procedure:* solve the *right* problem first (diverge/observe), then solve it right
(converge/prototype/test with real users). *Use when* requirements are assumed rather than
observed.

**Design for Error (Slips vs Mistakes)** — error is normal; design so it can't become a
disaster. *Procedure:* classify the error — a **slip** is the right plan executed wrong (add
better signifiers/feedback); a **mistake** is the wrong plan (fix the conceptual model). Then add
**forcing functions** (interlocks, confirmations on irreversible acts), constraints, sensible
defaults, and **undo**. *Use when* errors are frequent, costly, or irreversible.

## How to apply — decision procedure
1. **Reframe blame to design.** Restate "the user/agent got it wrong" as "the system made the
   wrong thing easy." Hunt for the system error.
2. **Walk the seven stages** on a real task; mark the stage that breaks.
3. **Diagnose the gulf.** Is the break in execution (can't act) or evaluation (can't tell)?
4. **Apply the six principles** at the break: add the missing signifier, mapping, constraint,
   or feedback; repair the conceptual model.
5. **Check discoverability + understanding.** Could a first-timer figure out what's possible and
   what's happening, with no manual?
6. **Design for the error.** Classify slip vs mistake; add forcing functions, constraints,
   defaults, and undo so the inevitable error is survivable.
7. **Test with real users (or real runs)**, observe, iterate.

## In the agentic world order
- **Tools are affordances; descriptions are signifiers.** An agent does only what its tools
  afford, and discovers them only through name + schema + docstring. A vague description is a
  hidden signifier — the "Norman door" of agents. Make the right call obvious.
- **The system prompt is the conceptual model.** Wrong behavior usually means the model in the
  prompt has diverged from the model the task needs. Fix the model, not the symptom.
- **Two gulfs → tool ergonomics + return values.** Execution gulf: can the agent express its
  intent in the tools you gave it? Evaluation gulf: does each tool return state legible enough
  for the agent to know what happened? Terse/ambiguous output causes loops and hallucinated
  success.
- **Design for error.** "The agent is dumb" is usually system error. Add constraints (typed
  args, allow-lists), forcing functions (confirmation on destructive calls), sensible defaults,
  and undo (dry-runs, reversible writes) so a bad call is survivable, not catastrophic.
- **Discoverability + understanding** become the agent's tool-discovery and observability story:
  can it find the right tool, and can it read what the tool did?

## Pitfalls
- Norman's own caution: don't blame the user (or agent) — most failures are design failures;
  resist the reflex to "train the human" when you should fix the system.
- **Affordance has been muddied** — Norman himself had to add "signifier" in 2013 because people
  misused "affordance" to mean "the cue." Keep them distinct: affordance = possible action,
  signifier = the perceptible cue. Don't let loose vocabulary hide a real gap.
- The book is **repetitive and example-heavy** (doors, stoves, light switches); the principles
  matter more than the anecdotes — extract the framework, skip the padding.
- It's **strong on diagnosis, weak on incentives.** It names that business pressure and feature
  creep cause bad design, then under-delivers on fixing that systemic problem — pair it with
  product/business judgment when incentives, not ignorance, are the cause.
- It's **light on emotion and aesthetics** (Norman addresses this later in *Emotional Design*);
  usability isn't the whole of a good experience.
- Its **everyday-object lens undersells complex, networked, software-first systems** — apply the
  principles, but expect harder edge cases in real distributed/agentic software.
