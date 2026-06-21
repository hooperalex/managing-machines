---
name: the-checklist-manifesto
description: Apply Atul Gawande's The Checklist Manifesto frameworks — the Simple/Complicated/Complex problem typology, ignorance vs. ineptitude, DO-CONFIRM vs. READ-DO checklists, defined pause points, the five-to-nine killer-item rule, and the team huddle (distributed authority). Use when designing or hardening a process, runbook, deploy, or review gate, reducing avoidable errors, building or auditing a checklist, deciding what to automate vs. keep under human judgment, or doing the equivalent while operating a fleet of AI agents.
---

# The Checklist Manifesto — Atul Gawande's frameworks, as a skill

Source: *The Checklist Manifesto: How to Get Things Right* (Atul Gawande, 2009). This skill
lets you **apply** Gawande's method, not just describe it. Extracted by Managing Machines,
Issue 020.

## When to use
- A skilled person or agent keeps dropping known, critical steps — failures of execution, not knowledge.
- You're designing or hardening a process, runbook, deploy, or review gate.
- You want to build, shorten, or audit an existing checklist.
- A complex, multi-party task needs the right specialists to communicate at the right moment.
- You're deciding what to automate vs. keep under human judgment.

## Core principle
**Most failure in complex work is ineptitude, not ignorance** — we know the right thing and
still fail to do it reliably. The volume of what we know has outrun any individual's ability
to deliver it. A short, well-built checklist is the cheapest defense: it guards the
"stupid but critical" steps so attention is freed for genuine judgment. The proof points are
hard to argue with — the WHO surgical checklist cut major complications ~36% and deaths ~47%
across eight hospitals; Pronovost's five-line central-line checklist nearly eliminated
catheter infections in Michigan ICUs.

## The frameworks

**Simple / Complicated / Complex** (Zimmerman & Glouberman typology) — classify the work before
choosing a tool. *Procedure:* label each part — Simple (a recipe; one repeatable path),
Complicated (a rocket; many simple parts plus expert coordination, still repeatable), or
Complex (raising a child; every instance differs, outcomes uncertain). Checklist the Simple
and Complicated steps; reserve human judgment for the Complex. *Use when* deciding what to
standardize vs. leave to discretion.

**Ignorance vs. Ineptitude** — diagnose the failure mode first. *Procedure:* for each failure,
ask "did we not know the right thing, or did we know it and not do it?" If ignorance, you need
research or expertise. If ineptitude, a smarter expert or model won't help — structure will.
*Use when* deciding whether more knowledge or more discipline is the fix.

**DO-CONFIRM vs. READ-DO** — match the checklist design to the work. *Procedure:* READ-DO =
read each item, then perform it, recipe-style (best for unfamiliar or linear tasks where order
matters). DO-CONFIRM = do the work from memory and expertise, then stop at a defined point to
confirm nothing critical was missed (best for experts in fast flow). Pick one per checklist;
don't blend. *Use when* authoring a checklist and choosing its format.

**Pause Points** — bind the checklist to an unmissable trigger. *Procedure:* name the exact
moment it runs (before incision, before the patient leaves the room, before merge). Tie it to
a hard, observable event — not "when you remember." Without a trigger, even a good checklist
silently stops being used. *Use when* a checklist exists but isn't reliably run.

**Five-to-Nine Killer Items** — keep it brutally short. *Procedure:* list only steps that are
both (a) actually missed in practice and (b) critical if missed. Cut everything obvious,
low-stakes, or already reliably done. Target ~5–9 items runnable in 60–90 seconds. *Use when*
a checklist is bloated, ignored, or slowing the work.

**The Team Huddle (Distributed Authority)** — make the checklist a communication act.
*Procedure:* at the pause point, have participants state names and roles, voice concerns
aloud, and explicitly empower the most junior person to stop the line. The list distributes
authority, not just steps. *Use when* the failure is silence or coordination, not a missing step.

## How to apply — decision procedure
1. **Name the failure.** Ignorance or ineptitude? Only proceed if it's ineptitude — structure is the fix.
2. **Classify the work.** Simple / Complicated / Complex. Checklist the first two; leave the third to judgment.
3. **Find the killer items.** Which critical-but-skippable steps actually get missed? Keep 5–9.
4. **Pick the design.** READ-DO for linear or unfamiliar work; DO-CONFIRM for expert flow.
5. **Set the pause point.** Bind the checklist to a hard, observable trigger.
6. **Add the huddle.** For multi-party work, build in a communication and permission-to-halt step.
7. **Test and trim.** Run it live, watch for friction, and cut anything that becomes a distraction.

## In the agentic world order
- **Ineptitude is the model's failure mode.** A capable agent that skips a known step is
  Gawande's surgeon. The fix is a short checklist in the prompt or workflow — not a bigger model.
- **DO-CONFIRM = the verification gate.** Let the agent reason freely inside the task (READ-DO),
  then force a pre-ship DO-CONFIRM it cannot skip: tests run? secrets scanned? scope respected?
  diff reviewed? Wire it to a hard pause point (pre-merge / pre-action hook).
- **Classify before automating.** Hand Simple and Complicated steps to the agent with a
  checklist; keep Complex, high-judgment calls human-in-the-loop. Don't checklist judgment;
  don't improvise what should be routine.
- **Five killer items, not fifty.** Per-run checklists should cover only what agents actually
  drop. Past the attention budget they get ignored — exactly as humans abandon long lists.
- **The huddle → distributed authority.** Give every reviewer (and the agent itself) explicit
  permission to halt a run when something looks wrong; surface roles and concerns before action,
  especially across a multi-agent fleet where no single agent sees the whole picture.

## Pitfalls
- **Gawande's own caution:** checklists fit predictable, procedural failures — they don't fix
  errors of judgment in genuinely complex situations. Don't reach for one where discernment is needed.
- **Bloat kills adoption.** A list past ~60–90 seconds or ~9 items becomes a distraction and
  gets abandoned. Shorter beats complete.
- **No pause point = no checklist.** Without a hard trigger it silently falls out of use.
- **Ego resistance is real.** Experts — and prompt authors who trust the model — feel the
  checklist is beneath them. Treat that resistance as the cost of reliability, not a reason to drop it.
- **From the critics:** the idea is narrow — a powerful tool, not a theory of everything. The
  book is light on *how* to build and maintain checklists, and its forays beyond medicine and
  aviation (e.g., investing) are its weakest. Build your own construction-and-maintenance
  process; don't expect the book to hand you one.
