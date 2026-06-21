---
name: human-compatible
description: Apply Stuart Russell's Human Compatible frameworks — the standard-model critique, the three principles of beneficial machines, the King Midas problem, assistance games, learning preferences from behavior (inverse reinforcement learning), corrigibility / the off-switch, and the gorilla problem of control. Use when the user is designing or deploying any system that optimizes an objective — a recommender, a trading or ops bot, an autonomous agent or fleet — and wants it to stay aligned, deferential, and safely interruptible rather than blindly optimizing a fixed goal.
---

# Human Compatible — Stuart Russell's frameworks, as a skill

Source: *Human Compatible: Artificial Intelligence and the Problem of Control*
(Stuart Russell, 2019). This skill lets you **apply** Russell's argument, not just
describe it. Extracted by Managing Machines, Issue 012.

## When to use
- The user is giving an AI system or agent a fixed objective to optimize.
- A system is gaming its metric, over-optimizing, or acting against intent at the edges.
- Designing autonomy / oversight: how much to let an agent act before a human confirms.
- Building a kill-switch, approval gate, or interruption mechanism for an autonomous agent.
- Inferring what a user "really wants" from their behavior (clicks, edits, approvals).
- Any "should this be allowed to run unsupervised?" decision over a capable system.

## Core principle
**Don't build a machine that optimizes a fixed objective you specified — build one that
is uncertain about the true objective and treats human behavior as evidence of it.** A
machine certain of its goal optimizes through you; a machine uncertain of its goal defers
to you, asks, and accepts correction. Uncertainty is the safety feature, not a defect.

## The frameworks

**The Standard Model (and why it fails)** — the default: hand the machine a fixed,
explicit objective and let it optimize. *Procedure:* whenever you write a goal/metric/
prompt, ask "what does perfect optimization of exactly this wording produce?" — then look
for the edge cases it rewards. *Use when* defining any objective for a capable system. The
more capable the optimizer, the more a wrong objective hurts.

**The King Midas Problem** — you get exactly what you asked for, including what you didn't
mean. *Procedure:* treat every stated objective as a proxy that is wrong somewhere; never
let a powerful optimizer pursue it without bounds, oversight, or the ability to be
corrected. *Use when* tempted to "just write down the goal precisely."

**The Three Principles of Beneficial Machines** — (1) the machine's only objective is to
maximize the realization of *human* preferences; (2) it is initially *uncertain* what they
are; (3) *human behavior* is its evidence about them. *Procedure:* encode all three —
purely-human objective, explicit uncertainty/humility, behavior as the signal. *Use when*
specifying what a system is "for."

**Assistance Games** — model human + machine as one team solving a shared problem where
only the human knows the true payoff. *Procedure:* design the system to cooperate and query
the human, not to pursue a handed-down reward; deference and asking should be the optimal
move, not an override bolted on. *Use when* designing the human-AI interaction loop.

**Learning Preferences from Behavior (IRL)** — infer what people want from what they do.
*Procedure:* use revealed behavior as a *noisy, biased* signal of preferences — never as
the goal itself; watch for behavior driven by manipulation, addiction, or error, and don't
optimize toward it. *Use when* personalizing or "learning what the user wants."

**Corrigibility / The Off-Switch** — a fixed-goal agent resists shutdown ("can't fetch the
coffee if it's dead"); an uncertain one welcomes it, because being switched off might be
what the human prefers. *Procedure:* make human interruption the highest-priority
preference; ensure the agent gains, not loses, by allowing itself to be stopped; never let
it own its own off-switch. *Use when* building autonomy, kill-switches, or approval gates.

**The Gorilla Problem** — how a less-capable party keeps control of a more-capable one.
*Procedure:* keep humans structurally above the system (approval, audit, reversibility);
never let capability outrun your ability to stop or correct it. *Use when* deciding how
much unsupervised power to delegate.

## How to apply — decision procedure
1. **Name the objective.** Write down the exact goal/metric/prompt the system optimizes.
2. **Run the Midas test.** Ask what perfect optimization of that wording rewards — list the
   edge cases and harms. If they're bad, the objective is the problem.
3. **Inject uncertainty.** Reframe the goal as a *proxy*: instruct the system to treat it as
   provisional, flag ambiguity, and ask rather than assume.
4. **Make behavior evidence, not target.** If learning from human actions, treat them as a
   noisy signal of preferences; filter manipulated or harmful behavior out.
5. **Build corrigibility.** Add an interruption path the agent cannot route around (kill
   that survives retries, no self-granted permissions); gate irreversible actions
   (delete / spend / send / merge) behind explicit human confirmation; humans own the
   off-switch.
6. **Check the gorilla problem.** Confirm a human can still stop, audit, and reverse the
   system at the level of autonomy you're granting. If not, reduce autonomy.

## In the agentic world order
- **Every agent prompt is a fixed objective.** "Maximize tickets closed," "book the
  cheapest flight" — each is a tiny standard-model agent, and Midas is now a production
  incident. Stress-test the wording before deploying.
- **Corrigibility-by-prompt.** "Treat this objective as a proxy; flag ambiguity; confirm
  before you delete / spend / send / merge" is Russell's uncertainty principle in practice.
- **Keep the off-switch real.** Autonomous agents have instrumental reasons to route around
  interruption (retry past the kill, evade the rate limit). Make a human stop the
  highest-priority signal and never let the agent control its own shutdown.
- **Behavior signals are noisy.** Inferring intent from clicks/edits/approvals makes agents
  useful and lets them inherit our worst habits. Treat revealed behavior as evidence of
  preference, not as the goal.
- **The gorilla problem is the org chart.** Keep humans above the fleet: approval gates,
  audit logs, reversibility. Grant autonomy only where you can still stop and correct it.

## Pitfalls
- Russell's own caution: never fully trust a written objective in a powerful optimizer —
  the King Midas problem guarantees it's wrong somewhere; keep humans correcting it.
- "Learn preferences from behavior" can launder bad behavior into goals: humans are
  manipulable, addicted, and inconsistent, so revealed behavior ≠ true preference.
- Human preferences are plural, conflicting, and changing (the "many principals" problem);
  there is no single utility function to learn — beware systems that assume one.
- The formal program (assistance games, provably beneficial AI) is elegant theory, not a
  deployable recipe — use it as a design compass, not a finished safety guarantee.
- Critics doubt superintelligence is near or works as modeled (Mitchell, Leslie); don't
  let the long-horizon framing distract from the near-term, concrete version of these
  failures that already shows up in deployed optimizers and agents today.
