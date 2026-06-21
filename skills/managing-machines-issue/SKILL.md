---
name: managing-machines-issue
description: Research a book in depth and produce a "Managing Machines" daily-newsletter issue (email-safe HTML + Markdown) AND extract the author's frameworks into an installable per-book skill. Use when the user wants to create a new Managing Machines issue, write up a book for the newsletter, turn a book into a skill, or extract an author's frameworks.
---

# Managing Machines — Issue Producer

This is the repeatable pipeline behind the **Managing Machines** newsletter
(*"Leadership, systems & deep work — reread for the people who run the agents."*).
Each run turns one book into **two** artifacts:

1. A newsletter **issue** — email-safe HTML (primary) + a Markdown copy.
2. An installable **book skill** — the author's frameworks distilled so an AI can *apply*
   them. This is what makes the newsletter worthwhile: every issue is also a capability.

The project lives at `C:\Users\hoope\simplebook`. Reference issue & template:
`issue-001-atomic-habits.html`. Backlog: `book-list.md`.

---

## Inputs

- **Book** (title + author). If not given, pick the next unshipped book from `book-list.md`.
- **Issue number** and **date** (default: next number after the latest issue, today's date).

---

## Step 1 — Research deep (multi-source)

Do NOT summarize from memory alone. Gather and cross-check:

- **The book's actual content** — core thesis, structure (parts/chapters), the author's
  named frameworks, key terminology, the strongest 3–5 quotes.
- **Reception** — what reviewers and practitioners praise; ratings.
- **Criticism** — the substantive, fair critiques (weak evidence, missing contexts,
  who it doesn't serve). The "Other Side" section depends on this being honest.
- **Context** — author background, what came before (intellectual lineage), related titles.

Use web search / fetch for current sources. Keep a short source list for your own QA.

## Step 2 — Extract the frameworks (structured)

This feeds BOTH the issue and the book skill. For each framework the author teaches,
capture:

- **Name** (the author's term).
- **What it is** — one sentence.
- **The procedure** — the actual steps a person follows to use it.
- **When to use it** — the trigger condition.
- **Agentic translation** — how it changes when AI agents do the work (this is the
  publication's signature lens). E.g. "habit of doing → habit of orchestrating & verifying."

Aim for 4–8 frameworks. These are the spine of the per-book skill in Step 5.

## Step 3 — Get a working cover

Use the **Open Library Covers API** (free, no key, reliable). NEVER use placeholder
services — they render blank.

```
https://covers.openlibrary.org/b/isbn/<ISBN-13>-L.jpg
```

Verify before shipping:
```
curl -s -o /dev/null -w "%{http_code} %{content_type}" "https://covers.openlibrary.org/b/isbn/<ISBN-13>-L.jpg"
```
Expect `200 image/jpeg`. Fallback: `https://covers.openlibrary.org/b/id/<COVER_ID>-L.jpg`.

## Step 4 — Write the issue

Copy `issue-001-atomic-habits.html` as the template and replace content. Keep it
**email-safe**: table layout, inline CSS, 600px width, no JavaScript, Outlook fallbacks,
color-scheme locked to light. Update masthead issue number, date strip, `<title>`, cover.

**Required structure** (hero + 6 sections):

- **Hero** — cover image, title, "author · year · genre", a hook quote, meta chips
  (read-time / rating / pages), and a "Read this if…" box.
- **01 — Key Takeaways** — 5–8 numbered, punchy insight bullets.
- **02 — Core Concepts** — the named frameworks from Step 2 + short definitions.
- **03 — The Book, Part by Part** — structural breakdown by part/chapter.
- **04 — Lines Worth Keeping** — 3 strong quotes.
- **05 — The Other Side** — opinions, fair criticism, and "read next".
- **06 — In the Agentic World Order** *(signature, tinted block)* — how the book's ideas
  adapt when AI agents do the work. Use the "agentic translation" notes from Step 2.
- **Skill footer** — a block announcing the installable book skill produced in Step 5
  (see the reference issue for the exact markup).

Then produce a **Markdown copy** (`issue-NNN-<slug>.md`) mirroring the same content.

**Design tokens** (keep consistent across issues): paper `#EFE9DE`, card `#FFFFFF`, ink
`#1C1917`, muted `#57534E`, accent `#B45309`, hairline `#E7E1D6`, signature tint `#FBF4E9`.
Display serif: Georgia. Body: system sans (-apple-system, Helvetica, Arial).

## Step 5 — Emit the book skill

Write `skills/<book-slug>/SKILL.md` using the **book-skill template** below. This converts
the Step 2 frameworks into an actionable skill an AI can invoke.

```
---
name: <book-slug>
description: Apply <author>'s <book> frameworks — <list the named frameworks>. Use when <trigger conditions>.
---

# <Book> — <Author>'s frameworks, as a skill

## When to use
<trigger conditions>

## The frameworks
For each framework: name, one-line what, the step-by-step procedure, when to use.

## How to apply (decision procedure)
A short ordered routine that picks the right framework for the user's situation and walks it.

## In the agentic world order
How to apply these frameworks to managing AI agents / fleets, not just personal work.

## Pitfalls
The author's own warnings + the fair criticisms from research.
```

## Step 6 — QA checklist

- [ ] Cover URL verified `200 image/jpeg`.
- [ ] All 6 sections present; criticism is honest, not fluff.
- [ ] Agentic section is specific to THIS book, not generic.
- [ ] Issue number, date, `<title>`, masthead all updated.
- [ ] HTML renders (open in browser); Markdown copy exists.
- [ ] Book skill written to `skills/<slug>/SKILL.md` with valid frontmatter.
- [ ] `book-list.md` row marked as shipped.

---

## Output files

- `issue-NNN-<slug>.html`  (primary — publish from this)
- `issue-NNN-<slug>.md`    (Markdown source)
- `skills/<slug>/SKILL.md` (the installable book skill)

## Publishing (reminder)

Substack is HTML-first: open the `.html` in a browser, select-all, copy, paste into the
Substack editor (formatting + cover carry over). This beats pasting raw Markdown.

## Installing the book skills

Develop skills here under `skills/`. To make one available in every Claude Code session,
copy its folder into `~/.claude/skills/` (Windows: `C:\Users\hoope\.claude\skills\`).
