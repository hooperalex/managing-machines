---
name: co-intelligence
description: Apply Ethan Mollick's Co-Intelligence frameworks — the four rules (invite AI to the table, be the human in the loop, treat AI like a person but tell it what kind, assume this is the worst AI you'll ever use), the jagged frontier, centaurs vs. cyborgs, AI as an alien intelligence, and the AI roles (person, creative, coworker, tutor, coach, future). Use when the user is adopting generative AI into real work, deciding what to delegate to AI, designing prompts/personas, setting up human oversight and review — or doing the equivalent while operating a fleet of AI agents.
---

# Co-Intelligence — Ethan Mollick's frameworks, as a skill

Source: *Co-Intelligence: Living and Working with AI* (Ethan Mollick, 2024). This skill lets
you **apply** Mollick's operating system, not just describe it. Extracted by Managing
Machines, Issue 003.

## When to use
- The user is folding generative AI into real work and wants a practical method.
- A delegation question: which parts of a task to give AI vs. keep human.
- Designing prompts, personas, or roles for an AI (or a fleet of agents).
- Setting up oversight: where humans must stay accountable for judgment and accuracy.
- Mapping where AI is reliable vs. unreliable for a specific kind of task.

## Core principle
**Treat AI as co-intelligence, not as a tool or a threat.** It is a new, "alien" kind of
intelligence that is neither a person nor ordinary software. You get the most from it by
working *with* it — inviting it into the work, keeping human judgment in charge, and
empirically learning the uneven boundary of what it can and can't do.

## The frameworks

**Rule 1 — Always invite AI to the table** — *what:* use AI for everything you legally and
ethically can, so you learn its real capabilities by doing. *Procedure:* for each task you
do, ask "could AI attempt this?"; try it; keep what works, discard what doesn't; build an
intuition no one can hand you. *Use when* you're unsure where AI helps — the answer is found
by probing, not predicting.

**Rule 2 — Be the human in the loop** — *what:* keep a person accountable for judgment,
accuracy, and the final call. *Procedure:* identify the cost of error; require human review
where it's high; fact-check confident-sounding output; never ship unverified AI claims in
high-stakes contexts. *Use when* AI output feeds a decision, a customer, or the record.

**Rule 3 — Treat AI like a person, but tell it what kind** — *what:* conversational,
role-laden prompting beats treating AI like a search box. *Procedure:* assign a clear
persona/role ("you are a skeptical editor…"), give context and examples, iterate
conversationally, ask it to critique or redo. *Use when* output is generic, shallow, or
off-target — the persona usually fixes it.

**Rule 4 — Assume this is the worst AI you'll ever use** — *what:* today's model is the
floor; capability rises fast. *Procedure:* design workflows and habits that improve
automatically as models improve; don't over-invest in workarounds for today's specific
weaknesses; re-test tasks that failed on older models. *Use when* planning anything that
will outlive the current model generation.

**The Jagged Frontier** — *what:* AI's ability is an uneven boundary; similar-looking tasks
land on opposite sides of "can / can't." *Procedure:* don't assume difficulty predicts
success; test each task type; keep a running map of where AI is reliable vs. not for your
work. *Use when* deciding whether to trust AI on a given task.

**Centaurs and Cyborgs** — *what:* two collaboration modes. *Centaur* = divide labor by
strength (clear hand-offs); *Cyborg* = blend fluidly within a task, passing work back and
forth. *Procedure:* pick centaur when the split is clean and stakes differ by subtask; pick
cyborg when the work is iterative and tightly interleaved. *Use when* structuring how you
and AI share a piece of work.

**AI as an alien intelligence** — *what:* the LLM is neither a human mind nor ordinary
software — a text-predictor with no understanding, memory of you, or stake in being right.
*Procedure:* exploit its strengths (tireless generation, breadth, instant role-play) while
distrusting human-shaped cues — confidence, fluency, "I checked" — that imply competence it
doesn't have; verify, don't infer reliability from tone. *Use when* its output *sounds*
authoritative and you're tempted to trust it on that basis.

**The Roles of AI** — *what:* AI as person, creative, coworker, tutor, coach, and a lens on
the future. *Procedure:* name the role you want for this task and prompt accordingly (e.g.
"tutor: quiz me on this until I can't get it wrong," "creative: give me ten divergent angles,
no filtering"). *Use when* choosing how to deploy AI for a goal — the role sets the behavior.

## How to apply — decision procedure
1. **Invite it in.** For the task at hand, try AI on it before assuming it can't help.
2. **Locate the frontier.** Is this task on the reliable side for AI, or unproven? Test cheaply.
3. **Pick the role.** Person, creative, coworker, tutor, or coach — name it.
4. **Cast the persona.** Give AI a specific role, context, and examples; prompt conversationally.
5. **Choose centaur vs. cyborg.** Clean split, or interleaved hand-offs?
6. **Set the human checkpoint.** Decide where a person must verify; scale rigor to the cost of error.
7. **Plan for the floor rising.** Build so the workflow improves as models do; re-test old failures.

## In the agentic world order
- **Invite the agent to the table — everywhere.** Route a slice of every workflow through an
  agent to discover empirically where it adds value. Map capability by deploying, not guessing.
- **Human in the loop → human on the loop.** A fleet is too large to supervise output by
  output. Move *onto* the loop: review gates, sampling, approval checkpoints, and escalation
  rules keep judgment accountable without you reading everything.
- **Jagged frontier → an eval suite.** Turn "where does it succeed/fail" into a per-task eval
  harness, then route each job to the side of the frontier the agent can actually handle.
- **Cast the persona at scale.** "Tell it what kind of person it is" becomes system-prompt and
  role design for each agent in the fleet.
- **Centaur/cyborg → orchestration shape.** Centaur = clean task hand-offs between specialized
  agents and humans; cyborg = tight human-agent interleaving on a single thread of work.
- **Worst AI you'll ever use → build for upgrades.** Design harnesses, tools, and guardrails
  that get better for free when the next model lands; avoid hard-coding around today's limits.

## Pitfalls
- **Author's caution — don't drop the human.** Rule 2 exists because AI is a fluent,
  confident fabricator; un-reviewed output in high-stakes settings is the central risk.
- **Author's caution — anthropomorphize carefully.** "Treat it like a person" is a usage
  tactic, not a claim about the machine; it's still an alien text-predictor, not a colleague
  with understanding or accountability.
- **The frontier is invisible and moving.** Don't generalize one success or failure; re-test
  as models change, and beware automation bias (over-trusting fluent answers).
- **From the critics — it can read as obvious and optimistic.** The frameworks are sticky but
  shallow; the book largely sets aside existential, accuracy, and job-displacement risk by
  design. Use it as a practical starter, and pair it with harder-edged risk and
  political-economy thinking for decisions with real stakes.
- **It dates fast.** A 2024 snapshot predates reasoning and agentic models; treat specific
  capability claims as a moving target, per Rule 4.
