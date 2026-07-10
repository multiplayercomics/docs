# Documentation project instructions

## About this project

- This is the documentation site for **Multic** — where you make and play
  interactive comics. Built on [Mintlify](https://mintlify.com).
- Pages are MDX files with YAML frontmatter. Configuration lives in `docs.json`.
- Run `mint dev` to preview locally. Run `mint broken-links` to check links.
- **All doc work happens on the `dev` branch.** `main` auto-deploys to
  docs.multic.com. Nothing reaches `main` without a human-reviewed PR.
- For Mintlify product knowledge (components, configuration), install the
  Mintlify skill: `npx skills add https://mintlify.com/docs`.

## Voice & style — READ FIRST

**`STYLE.md` is canon.** Read it before writing or editing any page. It defines
the voice (precise, clear, with measured play), the lexicon, the register map,
and where play is allowed. If your draft conflicts with `STYLE.md`, `STYLE.md`
wins.

The worked bar is `getting-started/what-is-a-multic.mdx` — match its quality.

## Terminology (non-negotiable)

- The content unit is **a Multic** (capitalised, countable). Never "video",
  "content", or "experience".
- You **make** Multics in **Studio**; people **play** them in the **Player**.
- The author is a **creator**; the audience is a **reader** (solo) or **player**
  (interactive/multiplayer).
- Node names are capitalised: **Frame**, **Dialogue**, **Narration**, **Choice**,
  **QTE**.
- Full lexicon and banned words: see `STYLE.md`.

## Style preferences

- Active voice, second person ("you"), present tense.
- Sentence case headings.
- Bold for UI elements (Open **Manage**); code formatting for files/paths/values.
- One idea per sentence; lead with the point.
- Avoid "simply", "just", "easily", "powerful", "seamless", "magic".

## Content boundaries

- This repo is **external/public** documentation only. Internal architecture,
  ops, billing internals, GTM, and demo playbooks live in the **separate private
  internal docs** — never put "our eyes only" material here.
- Don't document unreleased or internal-only features in public pages.

## How machine-assisted edits work

Docs are tiered (see `STYLE.md` → "How this stays handcrafted"):
- **Generated** (changelog, node/API reference, model & credit tables) may
  auto-commit to `dev`.
- **Assisted** feature pages: open a **draft PR** on `dev`; a human edits for
  voice and merges.
- **Handcrafted** voice-bearing pages: human/agent author, review required.

Always run `mint broken-links` before committing.
