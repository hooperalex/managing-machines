# Managing Machines — a daily book newsletter

*Leadership, systems & deep work — reread for the people who run the agents.*

One deeply-researched book per day, delivered as an email-safe HTML newsletter. Every issue
distills a great book on **productivity, management, teams, remote work, design thinking,
systems thinking, or learning from failure** — then reimagines it for a world where you
lead fleets of AI agents.

See `book-list.md` for the editorial backlog (the agentic-angle book queue).
(Working title/folder: SimpleBook.)

## What's here

- `issue-001-atomic-habits.html` — a fully-populated launch issue **and** your reusable
  template. Copy it, swap the content, ship. Built email-safe: table layout, inline CSS,
  600px width, no JavaScript, Outlook fallbacks, dark-mode locked to light.
- `issue-001-atomic-habits.md` — Markdown copy of the issue.
- `book-list.md` — the editorial backlog (agentic-angle book queue).
- `skills/` — the skill factory (see below).

## The newsletter is a skill factory

Every issue produces **two** things: a read, and an installable capability.

- **`skills/managing-machines-issue/`** — the *producer* skill. The repeatable, multi-step
  pipeline that researches a book, extracts the author's frameworks, writes the issue, and
  emits the per-book skill. Run it to make each new issue.
- **`skills/<book-slug>/`** — a *book* skill, one per issue. It distills the author's
  frameworks into something an AI can **apply**, not just summarize. Example shipped:
  `skills/atomic-habits/` (James Clear's Four Laws, habit stacking, Two-Minute Rule, etc.,
  including how to apply them to managing agent fleets).

Each issue ends with a "🧠 This issue ships a skill" block linking that book's skill — so
the newsletter doubles as a capability-install channel.

### Installing a skill (marketplace — recommended)

This repo is a **Claude Code plugin marketplace**. Each of the 30 books is its own plugin.
Add the marketplace once, then install any book:

```
/plugin marketplace add hooperalex/managing-machines
/plugin install atomic-habits          # or any book slug
```

Browse all 30 in [`skills/README.md`](./skills/README.md). The skill then activates by its
`description` trigger (e.g. ask to "build a habit" → `atomic-habits` kicks in).

**Manual install** (no marketplace): copy a folder into your global skills dir —
`cp -r skills/<slug> ~/.claude/skills/` (Windows: `C:\Users\hoope\.claude\skills\`).

> **Repo layout:** `skills/<slug>/` is the canonical source. `plugins/<slug>/` is the
> generated marketplace mirror (each plugin self-contains its skill, per the plugin spec)
> plus a `.claude-plugin/plugin.json`. The root `.claude-plugin/marketplace.json` lists all
> 30. Edit skills in `skills/`, then re-mirror into `plugins/` before publishing.

## The six sections in every issue

1. **Key Takeaways** — 5–8 punchy bullets
2. **Core Concepts** — named ideas + short definitions
3. **The Book, Part by Part** — chapter/section breakdown
4. **Lines Worth Keeping** — notable quotes
5. **The Other Side** — opinions, criticism & what to read next
6. **In the Agentic World Order** *(signature)* — how the book adapts when AI agents do the work

Plus a hero (cover, hook quote, "read this if…").

## Daily production workflow

1. **Pick the book.** One per day.
2. **Research deep** — not just the raw text: reviews, author context, common criticisms,
   related titles. (This is where AI does the heavy lifting on the newsletter copy.)
3. **Fill the template.** Replace the Atomic Habits content in the HTML. Update the masthead
   issue number (`No. 001`), the date strip, and the cover image (see below).
4. **Publish.**
   - **Substack (primary):** open the `.html` issue in a browser, select all (`Ctrl+A`),
     copy, and paste into the Substack editor. This carries the formatting over far better
     than pasting raw Markdown. The cover image comes across in the paste.
   - **Other ESPs** (Mailchimp, Buttondown, Beehiiv, Resend, etc.) accept the raw HTML
     directly. Keep `{{subscriber_id}}` style merge tags your ESP supports.

> **Format note:** HTML-first beats Markdown-first for the Substack paste workflow. The
> `.md` copy is kept only as a secondary source format.

## Book covers — the reliable method

Email and Substack need an **absolute, publicly-hosted** image URL. Don't use placeholder
services (e.g. `via.placeholder.com`) — they're flaky and render blank.

Use the **Open Library Covers API** — free, no key, stable:

```
https://covers.openlibrary.org/b/isbn/<ISBN>-L.jpg
```

- Find the ISBN-13 on the book's Open Library / Amazon page (Atomic Habits = `9780735211292`).
- `-L` = large; `-M` / `-S` also exist.
- Verify it returns a real image before shipping:
  `curl -s -o /dev/null -w "%{http_code} %{content_type}" "https://covers.openlibrary.org/b/isbn/9780735211292-L.jpg"`
  → should print `200 image/jpeg`.
- Fallback if a title has no ISBN cover: search openlibrary.org, grab the cover ID, and use
  `https://covers.openlibrary.org/b/id/<COVER_ID>-L.jpg`.

Always keep the descriptive `alt` text on the `<img>` for clients that block images.
