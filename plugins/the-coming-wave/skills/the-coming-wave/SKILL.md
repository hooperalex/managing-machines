---
name: the-coming-wave
description: Apply Mustafa Suleyman's The Coming Wave frameworks — the containment problem, the four features (asymmetry, hyper-evolution, omni-use, autonomy), Artificial Capable Intelligence (ACI) and the Modern Turing Test, the grand bargain, the narrow-path dilemma (catastrophe vs dystopia), pessimism-aversion, choke points, and the ten steps to containment. Use when the user is assessing the risk of a powerful technology, deciding whether and how to deploy AI or autonomous systems, designing guardrails/kill-switches, or governing a fleet of AI agents.
---

# The Coming Wave — Mustafa Suleyman's frameworks, as a skill

Source: *The Coming Wave* (Mustafa Suleyman with Michael Bhaskar, 2023). This skill lets you
**apply** Suleyman's containment lens, not just describe it. Extracted by Managing Machines,
Issue 007.

## When to use
- The user is assessing whether a powerful technology (AI, autonomous systems, bio, etc.) can be controlled.
- A deploy / don't-deploy decision where both action and inaction carry real risk.
- Designing guardrails, kill-switches, audits, or shutdown procedures.
- Governing or scaling a fleet of AI agents and deciding how much autonomy to grant.
- Spotting where an organization is looking away from uncomfortable risk (pessimism-aversion).

## Core principle
**Containment is the test that matters: can you monitor, curtail, control, and if necessary
shut down a technology at any stage of its life cycle?** If the answer is no, the technology
is uncontained — and the goal is to engineer "many locks," a defense-in-depth across
technical, cultural, legal, and political layers, rather than rely on any single safeguard.

## The frameworks

**The Four Features** — what makes a technology hard to contain. *Procedure:* score the tech
(or agent) on each — *asymmetry* (can a small actor cause outsized harm?), *hyper-evolution*
(how fast does it improve/iterate?), *omni-use* (how many unrelated good and bad uses?),
*autonomy* (can it act without a human in the loop?). More features lit up = harder to
contain = more locks required. *Use when* triaging how dangerous a capability is.

**Omni-use** — beyond "dual-use": general-purpose substrates ("the new electricity") usable
everywhere. *Procedure:* assume you cannot cleanly separate good uses from bad; contain at
the input/access layer, not the use-case layer. *Use when* someone proposes "we'll just ban
the bad uses."

**Artificial Capable Intelligence (ACI) / Modern Turing Test** — capability, not conversation,
is the bar. *Procedure:* test whether the system can autonomously achieve a complex
real-world goal end-to-end (Suleyman's example: turn $100k into $1M). Treat crossing that
bar as the trigger for tighter containment. *Use when* deciding if a system is "merely a
chatbot" or genuinely capable/autonomous.

**The Central Dilemma (Narrow Path)** — both deploying and refusing carry catastrophic risk;
there is no safe stop. *Procedure:* frame the choice as steering between two cliffs —
catastrophe (uncontained openness) and dystopia (control that becomes oppression) — and aim
for the narrow path between them rather than a binary yes/no. *Use when* the debate has
collapsed into "ship it" vs "ban it."

**Pessimism-Aversion** — the bias that makes people (especially elites) look away from dark
realities. *Procedure:* name it, then deliberately surface the worst-case scenarios you're
tempted to ignore; require the failure modes to be written down. *Use when* a plan feels
suspiciously optimistic or risk discussion is being waved off.

**Choke Points** — contain by controlling critical bottlenecks. *Procedure:* identify the
scarce inputs the capability depends on (compute, specialized chips, key materials, lab
access, data, credentials) and govern those, since they're easier to control than the
diffuse uses downstream. *Use when* the technology itself is too distributed to regulate
directly.

**Containment (Ten Steps)** — the layered program: technical safety ("Apollo program"),
choke points, open-source governance, biosecurity, international coordination (treaty-style),
corporate accountability/audits, regulation that keeps pace, a self-critical culture,
stronger institutions, and people power. *Procedure:* don't pick one — stack as many layers
as the risk warrants. *Use when* designing real safeguards rather than slogans.

## How to apply — decision procedure
1. **Score the four features.** Asymmetry, hyper-evolution, omni-use, autonomy — how lit up is this?
2. **Run the ACI test.** Is it genuinely capable/autonomous, or merely conversational? Capability raises the bar.
3. **Ask the containment question.** Can you monitor, curtail, control, and shut it down today? Where can't you?
4. **Name the dilemma.** State the catastrophe cliff and the dystopia cliff; aim for the narrow path, not a binary.
5. **Check for pessimism-aversion.** Write down the failure modes you're tempted to ignore.
6. **Find the choke points.** Which scarce inputs/permissions can you actually govern?
7. **Stack the locks.** Assemble defense-in-depth from the ten steps — never a single safeguard.

## In the agentic world order
- **Containment = a working kill-switch.** Fleet-sized containment is the ability to monitor,
  curtail, and stop any agent run. If you can't stop it, don't run it.
- **Autonomy is the dial you own.** Of the four features, autonomy is the one under your direct
  control — grant it incrementally, never by default.
- **ACI is your promotion gate.** Widen an agent's autonomy only when it has demonstrably
  achieved the real goal end-to-end on this task — capability, not vibes.
- **Choke points → permissions.** Govern at the input layer: scoped API keys, tool allow-lists,
  rate limits, and spend caps beat trusting the prompt.
- **Omni-use → assume misuse paths.** A general-purpose agent has uses you didn't intend;
  contain access, not just intended use-cases.
- **Beat pessimism-aversion.** Red-team the dark scenarios, keep a human in the loop on
  high-impact actions, and treat safeguards as defense-in-depth: evals, sandboxes, audits, shutdown.

## Pitfalls
- **Author's own caution:** containment under current conditions is *not* possible — treat any
  single safeguard as insufficient; the point is stacked, overlapping locks.
- **The narrow path cuts both ways:** over-containment slides toward dystopia/surveillance. Don't
  "solve" risk by centralizing so much control that you create a worse problem.
- **From the critics:** the book is long on alarm and short on implementation, and the ten steps
  can read as idealistic. Translate each step into a concrete, testable control before claiming it.
- **Author's conflict of interest:** Suleyman builds and sells the very technology he urges
  restraint on — read the prescriptions with that incentive in mind, and don't assume the
  framing is neutral.
- **Avoid technological determinism:** the book can imply tech evolves in one direction while
  society merely reacts. In practice your choices (what you deploy, how you gate it) shape the
  outcome — keep human agency and judgment in the loop.
