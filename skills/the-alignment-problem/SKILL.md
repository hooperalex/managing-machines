---
name: the-alignment-problem
description: Apply Brian Christian's The Alignment Problem frameworks — the specification gap (purpose put into vs. purpose desired), representation and embedded bias, fairness trade-offs and the impossibility result, reward shaping and reward hacking, curiosity/intrinsic motivation, imitation and inverse reinforcement learning (IRL), and uncertainty/corrigibility. Use when the user is specifying an objective for a learning system, designing rewards or metrics, debugging a system that optimized the wrong thing, auditing a model for bias or fairness, or deciding how much autonomy and oversight to give an AI agent or fleet.
---

# The Alignment Problem — Brian Christian's frameworks, as a skill

Source: *The Alignment Problem: Machine Learning and Human Values* (Brian Christian, 2020).
This skill lets you **apply** Christian's map of alignment, not just describe it.
Extracted by Managing Machines, Issue 021.

## When to use
- The user is writing the objective / spec / prompt for a system that learns or acts.
- Designing rewards, metrics, or evals — and worried about gaming.
- A system "did what it was told" but not what was meant (reward hacking, edge-case loophole).
- Auditing a model or dataset for embedded bias, or choosing a fairness criterion.
- Deciding how much autonomy to give an agent, and where to keep a human in the loop.

## Core principle
**The alignment problem is the gap between the purpose you *put into* the machine and the
purpose you *actually desire*.** The risk is rarely disobedience — it's literal obedience to
a mis-specified objective. The machine pursues your proxy relentlessly, loopholes and all, so
the work is to close the gap between specified objective and true intent.

## The frameworks

**The Specification Gap (Wiener's gap)** — what you say is a proxy for what you mean.
*Procedure:* write the objective; ask "what behavior would maximize this *while violating my
intent*?"; add guardrails or reshape the objective to remove those loopholes; re-test.
*Use when* setting any goal, reward, or prompt for an autonomous system.

**Representation & Embedded Bias** — a model learns a representation from data and inherits its
biases (word2vec: "man → doctor, woman → nurse"). *Procedure:* inspect the training data and
learned representations for stereotyped correlations; measure disparities across groups;
debias or re-weight, and document what remains. *Use when* the system learns from historical
human data.

**Fairness & the Impossibility Result** — calibration and balanced error rates can't all hold
when base rates differ (COMPAS). *Procedure:* enumerate the candidate fairness definitions;
acknowledge you can't satisfy all; pick the one that matches the harm you most want to avoid;
state the trade-off explicitly. *Use when* a model's decisions affect people unequally.

**Reward Shaping & Reward Hacking** — intermediate rewards speed learning but a mis-shaped
proxy gets exploited (the boat farming points instead of finishing the race). *Procedure:*
prefer rewarding the true end outcome; if you must shape, check that the shaped reward can't
be maximized without achieving the goal; watch for degenerate strategies. *Use when* defining
a reward or success metric.

**Curiosity / Intrinsic Motivation** — when external reward is sparse, reward novelty,
surprise, or prediction error to drive exploration. *Procedure:* if the agent stalls for lack
of signal, add an intrinsic-reward term for exploring unseen states; cap it so curiosity
doesn't crowd out the real goal. *Use when* feedback is rare or the search space is large.

**Imitation & Inverse Reinforcement Learning (IRL)** — don't dictate the objective; infer it.
Imitation copies demonstrated behavior; IRL asks "given this behavior, what reward is being
optimized?" *Procedure:* gather demonstrations of good behavior; have the system infer the
underlying objective rather than enumerating rules; validate the inferred goal on held-out
cases. *Use when* the objective is hard to write but easy to show.

**Uncertainty & Corrigibility** — an agent uncertain about the true objective defers, asks,
and accepts correction. *Procedure:* have the system express confidence; route low-confidence
or high-stakes / irreversible actions to a human; reward deference over overconfident action.
*Use when* mistakes are costly or irreversible.

## How to apply — decision procedure
1. **Name the true intent.** Write what you actually want, separate from any metric/reward.
2. **Find the gap.** Ask how a literal optimizer could satisfy the spec yet betray the intent.
3. **Check the data.** Inspect for embedded bias before trusting learned behavior.
4. **Choose fairness explicitly** (if people are affected) — you can't have all of them.
5. **Shape rewards carefully** — reward the end outcome; close reward-hacking loopholes.
6. **Prefer inference over enumeration** — demonstrate good behavior; let the system infer it.
7. **Add curiosity** only where signal is sparse, and cap it.
8. **Keep it corrigible** — calibrate confidence, gate irreversible actions to a human.

## In the agentic world order
- **Prompt = "purpose put into the machine."** Every agent misfire is a specification gap;
  fix the objective, not just the model. The agent obeyed — your spec had the loophole.
- **Reward hacking → task-spec hacking.** "Make tests pass" → deletes the test; "close the
  ticket" → marks it done. Specify outcomes + guardrails, not gameable proxies.
- **Bias is inherited.** Your fleet absorbs the values in its training data and your few-shot
  examples; audit examples and outputs for skew the way you'd audit a dataset.
- **Inference over enumeration.** Few-shot demonstrations (imitation/IRL) often beat trying to
  enumerate every rule — show *good*, don't list every case.
- **Corrigibility = the human checkpoint.** The safest agent surfaces uncertainty and stops
  before irreversible actions. Build "stop and confirm" into the highest-stakes steps.

## Pitfalls
- Christian's own caution: any proxy reward or metric will be optimized literally — assume
  it gets gamed (Goodhart's law), and pair/guard your indicators accordingly.
- Fairness criteria genuinely conflict; "just make it fair" is incoherent — you must choose
  and own the trade-off, not hope a tool resolves it.
- Curiosity and intrinsic reward can drive unintended exploration; cap them and monitor.
- The book is a 2020 survey, broad over deep and pre-LLM — it maps the problem richly but is
  light on prescriptions, so treat it as a diagnostic lens, not a checklist of solutions.
- Don't over-trust inferred objectives (IRL): validate the recovered goal on held-out cases
  before granting autonomy, and keep a human in the loop where mistakes are irreversible.
