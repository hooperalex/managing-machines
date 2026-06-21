# Managing Machines — Skills

Every issue of [Managing Machines](../README.md) ships an installable AI skill that distills
a book's frameworks into something an assistant can **apply**, not just summarize.

## Skills in this repo

**30 book skills** (one per issue) + the internal producer pipeline. Each book skill lets an
assistant *apply* the author's frameworks — to your own work and to managing agent fleets.

| # | Skill | Book / Author |
|---|-------|---------------|
| 001 | [`atomic-habits`](./atomic-habits/) | *Atomic Habits* — James Clear |
| 002 | [`high-output-management`](./high-output-management/) | *High Output Management* — Andy Grove |
| 003 | [`co-intelligence`](./co-intelligence/) | *Co-Intelligence* — Ethan Mollick |
| 004 | [`team-of-teams`](./team-of-teams/) | *Team of Teams* — Stanley McChrystal |
| 005 | [`thinking-in-systems`](./thinking-in-systems/) | *Thinking in Systems* — Donella Meadows |
| 006 | [`deep-work`](./deep-work/) | *Deep Work* — Cal Newport |
| 007 | [`the-coming-wave`](./the-coming-wave/) | *The Coming Wave* — Mustafa Suleyman |
| 008 | [`multipliers`](./multipliers/) | *Multipliers* — Liz Wiseman |
| 009 | [`sprint`](./sprint/) | *Sprint* — Jake Knapp |
| 010 | [`black-box-thinking`](./black-box-thinking/) | *Black Box Thinking* — Matthew Syed |
| 011 | [`the-effective-executive`](./the-effective-executive/) | *The Effective Executive* — Peter Drucker |
| 012 | [`human-compatible`](./human-compatible/) | *Human Compatible* — Stuart Russell |
| 013 | [`turn-the-ship-around`](./turn-the-ship-around/) | *Turn the Ship Around!* — L. David Marquet |
| 014 | [`the-goal`](./the-goal/) | *The Goal* — Eliyahu Goldratt |
| 015 | [`a-world-without-email`](./a-world-without-email/) | *A World Without Email* — Cal Newport |
| 016 | [`thinking-in-bets`](./thinking-in-bets/) | *Thinking in Bets* — Annie Duke |
| 017 | [`nexus`](./nexus/) | *Nexus* — Yuval Noah Harari |
| 018 | [`the-making-of-a-manager`](./the-making-of-a-manager/) | *The Making of a Manager* — Julie Zhuo |
| 019 | [`the-fifth-discipline`](./the-fifth-discipline/) | *The Fifth Discipline* — Peter Senge |
| 020 | [`the-checklist-manifesto`](./the-checklist-manifesto/) | *The Checklist Manifesto* — Atul Gawande |
| 021 | [`the-alignment-problem`](./the-alignment-problem/) | *The Alignment Problem* — Brian Christian |
| 022 | [`no-rules-rules`](./no-rules-rules/) | *No Rules Rules* — Reed Hastings & Erin Meyer |
| 023 | [`change-by-design`](./change-by-design/) | *Change by Design* — Tim Brown |
| 024 | [`superforecasting`](./superforecasting/) | *Superforecasting* — Philip Tetlock & Dan Gardner |
| 025 | [`the-4-hour-workweek`](./the-4-hour-workweek/) | *The 4-Hour Workweek* — Tim Ferriss |
| 026 | [`power-and-progress`](./power-and-progress/) | *Power and Progress* — Acemoglu & Johnson |
| 027 | [`remote-office-not-required`](./remote-office-not-required/) | *Remote* — Fried & Heinemeier Hansson |
| 028 | [`the-design-of-everyday-things`](./the-design-of-everyday-things/) | *The Design of Everyday Things* — Don Norman |
| 029 | [`the-year-without-pants`](./the-year-without-pants/) | *The Year Without Pants* — Scott Berkun |
| 030 | [`essentialism`](./essentialism/) | *Essentialism* — Greg McKeown |
| — | [`managing-machines-issue`](./managing-machines-issue/) | (internal) producer pipeline — research a book → emit issue + book skill |

## Install a skill (Claude Code)

These are standard Claude Code skills — a folder with a `SKILL.md`. To install one globally:

**Option A — copy one skill**
```bash
# macOS/Linux
cp -r skills/atomic-habits ~/.claude/skills/

# Windows (PowerShell)
Copy-Item -Recurse skills\atomic-habits "$env:USERPROFILE\.claude\skills\"
```

**Option B — clone the whole repo, then copy what you want**
```bash
git clone https://github.com/hooperalex/managing-machines.git
cp -r managing-machines/skills/atomic-habits ~/.claude/skills/
```

Once installed, the skill activates by its `description` trigger — e.g. ask your assistant
to help you *build a habit* and the `atomic-habits` skill kicks in.

Repo: https://github.com/hooperalex/managing-machines
