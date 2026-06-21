---
name: thinking-in-bets
description: Apply Annie Duke's Thinking in Bets frameworks — decisions as bets, separating decision quality from outcome ("resulting"), calibrated confidence and "I'm not sure", truthseeking pods and the CUDOS norms, and mental time travel (10-10-10, backcasting, premortems). Use when the user is making a consequential call under uncertainty, reviewing a decision after the fact, calibrating confidence, designing a review/dissent process — or doing the equivalent while operating a fleet of AI agents.
---

# Thinking in Bets — Annie Duke's frameworks, as a skill

Source: *Thinking in Bets: Making Smarter Decisions When You Don't Have All the Facts*
(Annie Duke, 2018). This skill lets you **apply** Duke's decision toolkit, not just
describe it. Extracted by Managing Machines, Issue 016.

## When to use
- A consequential decision must be made with incomplete information and real luck involved.
- A post-mortem: someone is grading a decision by how it turned out ("resulting").
- Calibrating or expressing confidence — turning true/false beliefs into probabilities.
- Designing a review, dissent, or feedback process that resists motivated reasoning.
- Deciding how much autonomy to grant an agent, or how to evaluate agent runs.

## Core principle
**Separate decision quality from outcome quality.** Life is poker, not chess: results are
produced by *both* the quality of your decisions *and* luck. A good process can lose and a
bad one can win, so judge the bet, not the result. Every decision is "a decision about an
uncertain future" — a bet — so make the odds and your confidence explicit.

## The frameworks

**Resulting (decision vs. outcome)** — the reflex to equate a decision's quality with its
result. *Procedure:* when reviewing, ask "was this a bad decision or a bad outcome?";
reconstruct what was knowable at decision time; grade the *process*, not the score; only
update the process when you see a repeatable error, not a single unlucky draw. *Use when*
celebrating a win or blaming a loss.

**Decisions as Bets / "Wanna Bet?"** — every choice wagers resources on one uncertain
future over alternatives (including future versions of yourself). *Procedure:* state the
decision as a bet; ask "Wanna bet?" of your own belief to expose hidden uncertainty;
estimate the odds and the payoff of each option. *Use when* a belief feels like a certainty
or a choice feels obvious.

**Calibrated Confidence / "I'm Not Sure"** — replace true/false with degrees of belief.
*Procedure:* attach a probability to claims ("I'm 70% sure"); treat "I'm not sure" as a
strength, not a weakness; when new evidence arrives, move the number rather than defending
the binary. *Use when* stating beliefs, forecasting, or arguing.

**Truthseeking Pods + CUDOS** — a chosen group accountable to *accuracy*, not agreement,
that catches the motivated reasoning you can't see in yourself. *Procedure:* recruit people
who reward truth over comfort; run on Merton's CUDOS norms — **C**ommunism (share all the
data), **U**niversalism (judge the claim, not the source), **D**isinterestedness (guard
against conflicts), **O**rganized **S**kepticism (welcome dissent and stress-test ideas).
*Use when* a decision is high-stakes or you suspect you're fooling yourself.

**Mental Time Travel** — recruit your past and future selves into the present decision.
*Procedure:* **10-10-10** — how will I feel about this in 10 minutes / 10 months / 10 years?
**Backcasting** — stand in a future where it succeeded and trace how; **Premortem** — stand
in a future where it failed and list why. Map both the positive and negative space before
committing. *Use when* a decision is emotional, irreversible, or you're in-the-moment.

## How to apply — decision procedure
1. **Reframe as a bet.** State the decision as a wager on an uncertain future; name the live options.
2. **Strip out resulting.** If reviewing, judge the *process* given what was knowable at the time, not the result.
3. **Put odds on it.** Estimate probabilities and payoffs for each option; say how sure you are ("70%"), and name where you're "not sure."
4. **Time-travel.** Run 10-10-10, backcast the success, and premortem the failure; fold the findings into the options.
5. **Pod it.** Run high-stakes calls past a truthseeking group under CUDOS; actively invite the strongest dissent.
6. **Decide and log the bet.** Record the decision, the confidence, the reasoning, and what would change your mind — so later you can grade the process, not the outcome.
7. **Field the outcome.** When results arrive, sort luck vs. skill; update the process only on repeatable signal, not one draw.

**Decision-log template** (capture at step 6, revisit at step 7):
```
Decision: <the bet, stated as a wager between named options>
Confidence: <e.g. 70%>   Not sure about: <the live unknowns>
Reasoning: <why this option beats the alternatives, given what's knowable now>
Premortem: <top 2-3 ways this fails> → Guardrails: <what catches each>
Disconfirm: <evidence that would flip this decision>
--- field later ---
Outcome: <what happened>   Luck or skill: <which, and why>
Process change: <only if the error is repeatable>
```

## In the agentic world order
- **Stop resulting on agents.** One passing (or failing) run is sample size 1 — luck, not
  proof. Grade the agent's *process* (reasoning, tool calls, retrieval), not the single output.
- **Every dispatch is a bet.** Treat each run as a wager with explicit odds; log a confidence
  before you ship it. An eval suite is a calibration curve — pass-rate over many runs is the
  fleet's real skill signal.
- **Reward "I'm not sure."** Prefer agents that surface calibrated uncertainty and abstain
  over ones that confabulate with false confidence; route low-confidence cases to a human.
- **Premortem the deploy; backcast the win.** Before granting autonomy, imagine the failure
  modes and turn them into guardrails and tests; imagine the success and trace the path into a spec.
- **Truthseeking pod → multi-model jury.** Use adversarial agents or a multi-model review
  bound to accuracy, not consensus, applying CUDOS — share full context, judge the claim not
  the model, and organize skepticism — to catch motivated reasoning one model won't see in itself.
- **Field outcomes into the process.** Feed graded runs back into prompts/evals only when the
  error is repeatable; don't overfit the system prompt to one unlucky trace.

## Pitfalls
- Duke's own caution: don't over-rotate on any single outcome — separate signal (skill) from
  noise (luck) before you "learn" from it, or you'll learn the wrong lesson.
- Motivated reasoning is invisible from the inside; without a real truthseeking pod and genuine
  dissent, self-review just rationalizes the bet you already wanted to make.
- The poker metaphor strains on decisions with moral stakes, relationship dynamics, or genuinely
  unquantifiable odds — don't force a probability where one doesn't honestly exist.
- The core idea is sharp but thin; the book is light on the *mechanics of behavior change*.
  Knowing to separate decisions from outcomes doesn't make you do it — build the habit into
  checklists, logs, and review rituals, not willpower.
- Beware cherry-picking: the framework is easiest where odds are clean. Apply it most carefully
  exactly where skill, luck, process, and outcome are hardest to disentangle.
