---
name: the-checklist-manifesto
description: Apply Atul Gawande's The Checklist Manifesto frameworks — the simple/complicated/complex problem typology, ignorance vs. ineptitude, DO-CONFIRM vs. READ-DO checklists, defined pause points, the five-to-nine "killer item" rule, and the team-huddle (distributed authority) move. Use when the user is designing a process, hardening a deploy/runbook, reducing avoidable errors, building or auditing a checklist, or doing the equivalent while operating a fleet of AI agents.
---

# The Checklist Manifesto — Atul Gawande's frameworks, as a skill

Source: *The Checklist Manifesto: How to Get Things Right* (Atul Gawande, 2009). This skill
lets you **apply** Gawande's method, not just describe it. Extracted by Managing Machines,
Issue 020.

## When to use
- A skilled person/agent keeps dropping known, critical steps (failures of execution, not knowledge).
- You're designing or hardening a process, runbook, deploy, or review gate.
- You want to build, shorten, or audit an existing checklist.
- A complex, multi-party task needs the right specialists to communicate at the right moment.
- You're deciding what to automate vs. keep under human judgment.

## Core principle
**Most failure in complex work is ineptitude, not ignorance** — we know the right thing and
still fail to do it reliably. The volume of what we know has outrun any individual's ability
to deliver it. A short, well-built checklist is the cheapest defense: it protects the
"stupid but critical" steps so attention is freed for genuine judgment.

## The frameworks

**Simple / Complicated / Complex** — classify the problem before choosing a tool. *Procedure:*
label the work — Simple (a recipe; repeatable), Complicated (a rocket; many simple parts +
expert coordination, still repeatable), or Complex (raising a child; every instance differs,
outcomes uncertain). Checklist the Simple and Complicated steps; reserve human judgment for
the Complex. *Use when* deciding what to standardize vs. leave to judgment.

**Ignorance vs. Ineptitude** — diagnose the failure mode. *Procedure:* ask "did we not know,
or did we know and not do it?" If ineptitude, a smarter expert/model won't help — a checklist
will. *Use when* deciding whether more expertise or more structure is the fix.

**DO-CONFIRM vs. READ-DO** — pick the checklist design. *Procedure:* READ-DO = read each item
and perform it, recipe-style (good for unfamiliar/linear tasks). DO-CONFIRM = do the work from
memory/expertise, then pause to verify nothing was missed (good for experts in fast flow).
*Use when* you're authoring a checklist and must match it to how the work actually runs.

**Pause Points** — give the checklist a trigger. *Procedure:* define the exact moment it
runs (before incision, before the patient leaves the room, before merge). Tie it to an
unmissable event; without a hard trigger, checklists get skipped. *Use when* a good checklist
exists but isn't being used.

**Five-to-Nine Killer Items** — keep it brutally short. *Procedure:* list only the steps that
(a) are actually missed and (b) are critical; cut everything obvious or low-stakes; target
~5–9 items runnable in 60–90 seconds. *Use when* a checklist is bloated, ignored, or
slowing people down.

**The Team Huddle (Distributed Authority)** — make the checklist a communication act.
*Procedure:* at the pause point, have the team state names/roles and voice concerns aloud,
and explicitly empower the most junior person to stop the line. *Use when* the failure is
coordination or silence, not a missing step.

## How to apply — decision procedure
1. **Name the failure.** Ignorance or ineptitude? If ineptitude, proceed; structure is the fix.
2. **Classify the work.** Simple / Complicated / Complex — checklist the first two only.
3. **Find the killer items.** What critical-but-skippable steps actually get missed? Keep 5–9.
4. **Pick the design.** READ-DO for linear/unfamiliar; DO-CONFIRM for expert flow.
5. **Set the pause point.** Bind the checklist to an unmissable trigger.
6. **Add the huddle.** Build in a communication/permission-to-halt step for multi-party work.
7. **Test and trim.** Run it live, watch for friction, cut anything that becomes a distraction.

## In the agentic world order
- **Ineptitude is the model failure mode.** A capable agent that skips a known step is
  Gawande's surgeon. The fix is a short checklist in the prompt/workflow, not a bigger model.
- **DO-CONFIRM = the verification gate.** Let the agent reason freely (READ-DO inside the
  task), then force a pre-ship DO-CONFIRM: tests run? secrets scanned? scope respected?
  diff reviewed? Make it a hard pause point the agent cannot skip.
- **Classify before automating.** Hand Simple/Complicated steps to the agent with a checklist;
  keep Complex, high-judgment calls human-in-the-loop. Don't checklist judgment; don't
  improvise what should be routine.
- **Five killer items, not fifty.** Per-run checklists should cover only what agents actually
  drop — bloat past attention and they get ignored, exactly as humans abandon long lists.
- **The huddle → distributed authority.** Give every reviewer (and the agent itself) explicit
  permission to halt a run when something looks wrong; surface roles and concerns before action.

## Pitfalls
- **Gawande's own caution:** checklists fit predictable, procedural failures — they don't
  fix errors of judgment in genuinely complex situations. Don't reach for one where
  discernment is needed.
- **Bloat kills adoption.** A list past ~60–90 seconds or ~9 items becomes a distraction and
  gets abandoned. Shorter beats complete.
- **No pause point = no checklist.** Without a hard trigger it silently stops being used.
- **Ego resistance is real.** Experts (and prompt authors who trust the model) feel the
  checklist is beneath them; treat that resistance as the cost of reliability, not a signal to drop it.
- **From the critics:** the idea is narrow — it's a powerful tool, not a theory of everything.
  The book is light on *how* to build and maintain checklists, and its forays beyond
  medicine/aviation (e.g., investing) are the weakest. Build your own construction process;
  don't expect the book to hand you one.
