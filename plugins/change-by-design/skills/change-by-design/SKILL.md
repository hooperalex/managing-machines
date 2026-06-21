---
name: change-by-design
description: Apply Tim Brown's Change by Design frameworks — the three constraints (desirability/feasibility/viability), the three spaces of innovation (inspiration/ideation/implementation), human-centered insight (observation/empathy/insight), divergent/convergent thinking, prototyping ("building to think"), the design brief, and T-shaped multidisciplinary teams. Use when the user is doing innovation or product work, framing a fuzzy problem, running ideation or research, deciding what to build, prototyping to learn — or doing the equivalent while designing and operating a fleet of AI agents.
---

# Change by Design — Tim Brown's frameworks, as a skill

Source: *Change by Design* (Tim Brown, 2009). This skill lets you **apply** Brown's
design-thinking operating system, not just describe it. Extracted by Managing Machines, Issue 023.

## When to use
- The user has a fuzzy, human problem and needs a repeatable process to turn it into something people want.
- Deciding *what* to build (or *whether* to build it) — separating "feasible" from "worth doing."
- Running discovery research, ideation/brainstorming, or prototyping.
- Framing an innovation effort as a project with a brief.
- Designing or operating AI agents that have to meet a real user need.

## Core principle
**Innovation succeeds at the overlap of desirability, feasibility, and viability — and you
get there by a repeatable, human-centered, prototype-driven process, not a flash of genius.**
Lead with the human need; make ideas tangible early; loop instead of marching in a straight line.

## The frameworks

**The Three Constraints (Desirability · Feasibility · Viability)** — durable innovation sits
where human desire, technical possibility, and business sustainability overlap. *Procedure:*
state the human need first (desirability); then ask what's technically possible now
(feasibility); then what's sustainable as a business/operation (viability); push the idea
toward the intersection of all three. *Use when* prioritizing ideas or killing ones that are
merely possible.

**The Three Spaces of Innovation (Inspiration · Ideation · Implementation)** — overlapping
spaces, not sequential stages. *Procedure:* inspiration = the problem/opportunity that
motivates the search (go observe); ideation = generate, test, and refine ideas; implementation
= the path to people's hands. Expect to loop back to an earlier space when you learn something.
*Use when* structuring an innovation project end-to-end.

**Human-Centered Insight (Observation · Empathy · Insight)** — insight is the raw material.
*Procedure:* observe real people in context (especially extreme users), build empathy for
their frustrations and motivations, then synthesize observations into insight about latent
needs they can't articulate. *Use when* you're tempted to design from your own assumptions or
from "the average user."

**Divergent / Convergent Thinking** — creativity is a rhythm of expansion then choice.
*Procedure:* first diverge — multiply options without judging (IDEO brainstorm rules: defer
judgment, encourage wild ideas, build on the ideas of others, stay focused on the topic, one
conversation at a time, go for quantity); then converge — make decisive choices against your
criteria. Never run both moves at once. *Use when* a team jumps to the first idea or can't
decide.

**Prototyping / "Building to Think"** — make the idea tangible to learn from it. *Procedure:*
build the roughest artifact that answers your biggest open question; test it; fail early and
cheaply; refine. "Fail early to succeed sooner." *Use when* an idea is being debated in the
abstract instead of being tried.

**The Design Brief** — a starting point and a set of constraints, not a fixed spec.
*Procedure:* write a brief with enough constraint to give direction and enough freedom to
discover; treat innovation as a finite project. *Use when* kicking off work; revisit the brief
as you learn.

**T-Shaped, Multidisciplinary Teams** — staff with people deep in one discipline and broad
enough to collaborate across many. *Procedure:* assemble a small, agile, interdisciplinary
team; favor "all of us are smarter than any of us" over expert handoffs across silos. *Use
when* composing the team.

## How to apply — decision procedure
1. **Frame the brief.** State the human problem and a few constraints; resist over-specifying the solution.
2. **Inspire from observation.** Go to real users (especially extremes); build empathy; harvest insights about latent needs.
3. **Diverge.** Generate many options against the insight, judgment deferred.
4. **Prototype to think.** Make the strongest few tangible fast; test; let early failure teach you.
5. **Converge.** Choose against desirability → feasibility → viability, in that order of inquiry.
6. **Implement & loop.** Ship toward people's hands; when you learn something, loop back to the right space rather than forcing the line.

## In the agentic world order
- **Three constraints → spec the agent at the overlap.** Don't ship an agent because it's
  newly *feasible*. Anchor on a real human need (desirability) and a sustainable
  cost/latency/risk envelope (viability). Build the fleet that sits in the intersection.
- **Three spaces → the build loop.** Inspiration (observe where humans struggle) → ideation
  (draft prompts/tools/traces) → implementation (ship behind a gate) is not a waterfall. Eval
  results constantly send you back to an earlier space.
- **Observation/empathy → ground on real traces, not averages.** Mine real interaction logs and
  the long tail (weird, angry, edge-case inputs) for latent needs before writing the system
  prompt. The average-tuned agent fails exactly where users needed it most.
- **Diverge/converge → fan out then judge.** Generate many candidates (multiple agents,
  sampling, temperature); then converge with a decisive selector or LLM-judge. Keep the two
  moves distinct.
- **Build to think → prototype the prompt, fail cheap.** A rough agent run against ten real
  cases teaches more than a perfect spec. Make behavior tangible fast; let early eval failure
  drive iteration.
- **T-shaped teams → multi-agent ensembles.** Specialist agents (deep) plus a generalist
  orchestrator (broad) that integrates across them.

## Pitfalls
- Brown's own caution: insight must come from *real people*, not the project team's assumptions —
  don't let a workshop shortcut actual user contact.
- The book gives the method in roughly its first half and an IDEO showcase after; it stops short
  of a concrete activity sequence — pair it with a hard blueprint (e.g. a design sprint) when you
  need step-by-step execution.
- Design thinking is easiest in creative consultancies and harder to embed in established orgs;
  budget for the politics, power, and operational reality the method tends to gloss over.
- The optimism can mask execution risk. "Fail early" is cheap only if failures are genuinely
  small and learning is captured — otherwise it's just churn. Keep prototypes cheap and the loop
  honest.
