# Managing Machines — Skills

Every issue of [Managing Machines](../README.md) ships an installable AI skill that distills
a book's frameworks into something an assistant can **apply**, not just summarize.

## Skills in this repo

| Skill | From | What it does |
|-------|------|--------------|
| [`atomic-habits`](./atomic-habits/) | *Atomic Habits* — James Clear | Apply the Four Laws, habit stacking, the Two-Minute Rule, identity-based habits — for personal habits and for managing agent fleets. |
| [`managing-machines-issue`](./managing-machines-issue/) | (internal) | The producer pipeline that researches a book and emits a new issue + book skill. |

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
git clone https://github.com/<owner>/<repo>.git
cp -r <repo>/skills/atomic-habits ~/.claude/skills/
```

Once installed, the skill activates by its `description` trigger — e.g. ask your assistant
to help you *build a habit* and the `atomic-habits` skill kicks in.

> Replace `<owner>/<repo>` once the GitHub repo exists.
