---
name: superforecasting
description: Apply Philip Tetlock & Dan Gardner's Superforecasting frameworks — the Ten Commandments, Fermi-izing (decomposition), the outside view vs. inside view, the dragonfly eye (perspective aggregation), Brier-score calibration vs. resolution, belief-updating, and perpetual beta. Use when the user is forecasting, estimating probabilities, making a high-stakes judgment call under uncertainty, scoring past predictions, designing a decision/eval process — or doing the equivalent while operating a fleet of AI agents.
---

# Superforecasting — Tetlock & Gardner's frameworks, as a skill

Source: *Superforecasting: The Art and Science of Prediction* (Philip Tetlock & Dan
Gardner, 2015), built on the Good Judgment Project tournament. This skill lets you
**apply** the superforecasters' method, not just describe it. Extracted by Managing
Machines, Issue 024.

## When to use
- The user is forecasting or assigning a probability to an uncertain future event.
- A high-stakes judgment call where being "less wrong" matters more than sounding sure.
- Scoring or post-morteming past predictions (was that 70% call actually good?).
- Designing a decision process, an eval rubric, or a confidence-reporting standard.
- Aggregating disagreeing experts, models, or agents into one estimate.

## Core principle
**Good judgment is a measurable, trainable skill — not innate genius or inside access.**
Translate vague hunches into numeric probabilities, track them against outcomes, and
update relentlessly. The strongest predictor of accuracy is *perpetual beta*: the
commitment to keep revising your beliefs — about three times as predictive as raw IQ.

## The frameworks

**The Ten Commandments** — Tetlock's experimentally-supported checklist. *What:* a
condensed operating procedure for any forecast. *Procedure:* (1) triage — spend effort
on Goldilocks-zone questions, not the trivial or the hopeless; (2) break problems into
tractable sub-problems; (3) balance outside and inside views; (4) update on new evidence;
(5) weigh clashing causal forces rather than picking one story; (6) granulate probabilities
(distinguish 55% from 60%); (7) balance under- and over-confidence; (8) learn from errors
without blame or hindsight bias; (9) bring out the best in teams; (10) treat the rules as
guidelines, not gospel. *When:* any non-trivial forecast — use it as a literal checklist.

**Fermi-izing** — *What:* decompose an intimidating question into estimable pieces.
*Procedure:* split the question into knowable and unknowable sub-quantities; assign an
explicit number to each assumption; recombine. *When:* the question feels too big or too
vague to answer directly — Fermi-izing "flushes ignorance into the open."

**Outside View → Inside View** — *What:* anchor on base rates before case specifics.
*Procedure:* name the reference class ("how often does this sort of thing happen?"), get
that base rate, *then* adjust up or down for what's distinctive about this case. *When:*
the situation feels unique or a vivid narrative is pulling your estimate — do outside first.

**Dragonfly Eye** — *What:* synthesize many independent perspectives into one view.
*Procedure:* gather genuinely different sources/models/people; actively solicit dissent;
aggregate rather than pick a favorite; let disagreement widen your uncertainty. *When:*
the question is contested or one viewpoint is dominating.

**Calibration vs. Resolution (Brier score)** — *What:* two separable components of accuracy.
*Procedure:* log every forecast as (probability, binary outcome). Compute the Brier score =
mean of (probability − outcome)² across resolved calls; lower is better (0 = perfect, 0.25 =
a coin flip on a 50/50, 1 = confidently wrong). Bucket forecasts by stated probability to see
*calibration* (do your "70%" events resolve ~70% true?) separately from *resolution* (are you
decisive, i.e. willing to leave 50%?). *When:* you want to measure and improve skill over time.

**Belief-Updating** — *What:* incremental Bayesian revision. *Procedure:* on each new piece
of evidence, nudge the probability — small steps, not switches; avoid both under-reaction
(anchoring) and over-reaction (chasing noise). *When:* a forecast is live and evidence is
arriving. Beliefs are hypotheses to be tested, not treasures to be guarded.

**Perpetual Beta** — *What:* a growth mindset toward your own judgment. *Procedure:* keep a
decision journal; revisit and rescore old calls; treat your method as software that's never
"done." *When:* always — it's the meta-trait that drives all the others.

## How to apply — decision procedure
1. **Triage.** Is this question in the Goldilocks zone (effort can move accuracy)? If trivial
   or hopeless, say so and stop.
2. **Fermi-ize.** Break it into sub-questions; mark each knowable vs. unknowable.
3. **Outside view.** Find the base rate of the reference class. Write it down first.
4. **Inside view.** Adjust for case specifics — deliberately, with reasons.
5. **Dragonfly eye.** Pull in independent perspectives/models; seek the strongest counter-case.
6. **State a granular probability** (e.g. 63%, not "likely") with an explicit horizon and a
   resolution criterion.
7. **Update** as evidence arrives, in small steps.
8. **Score it** (Brier) when it resolves; log the lesson without hindsight bias (perpetual beta).

## In the agentic world order
- **Make agents keep score.** Require agents to emit numeric confidence, then Brier-score
  them against outcomes. A calibrated agent can be trusted to act; an uncalibrated one is a
  confident guesser. Calibration is a precondition for autonomy.
- **Fermi-ize the prompt.** Decompose a hard task into estimable sub-questions an agent can
  actually answer, instead of asking for one heroic leap.
- **Dragonfly eye → ensembles.** Run several independent agents/models and aggregate; the
  spread of their answers is itself a real uncertainty signal. Diversity beats one clever model.
- **Outside view → anti-hallucination guardrail.** Force the base-rate question ("how often
  does this kind of claim/task hold?") before the agent commits to a vivid inside-view story.
- **Belief-updating → small, reversible actions.** Have agents act in steps that update on
  feedback rather than committing hard and early on a thin prior.
- **Perpetual beta → the eval loop.** Treat prompts, tools, and policies as never "done":
  measure, revise in small increments, and reward graceful revision over early certainty.

## Pitfalls
- **One-metric tunnel vision (author's own caveat).** The whole method optimizes the Brier
  score over short, resolvable questions. It transfers poorly to long-horizon, structurally
  novel, or genuinely one-shot events where base rates barely exist — don't over-apply it.
- **Knowing ≠ manufacturing.** Knowing what superforecasting is doesn't reliably tell you how
  to turn someone (or an agent) into one; the training-to-impact link is thinner than the
  confident tone implies. Treat results as directional, not guaranteed.
- **Robustness is partly open.** Team-with-aggregation vs. prediction-market comparisons and
  the unpublished raw distributions leave honest room for doubt. Hold conclusions provisionally.
- **Commandment 10 is load-bearing.** The rules are guidelines, not gospel — over-literal
  application (false precision, base-rate worship when the reference class is wrong) backfires.
- **Resolution criteria must be crisp.** A forecast you can't unambiguously score later teaches
  you nothing; always pin the exact event and horizon before predicting.
