# Multic documentation — voice & style guide

This is the source of truth for how Multic's documentation reads. Every page —
handcrafted or machine-assisted — is measured against it. If a sentence breaks a
rule here, the rule wins.

---

## What Multic is (say it the same way every time)

Multic is where you **make and play interactive comics** — branching, animated,
voiced, and playable with friends.

- The thing you create is **a Multic** (always capitalised, always countable —
  "make a Multic", "publish your first Multic", "play a Multic"). It is never a
  "video", "story-video", "piece of content", or "experience".
- You create in **Studio** (on the web). People read and play in the **Player**
  (on their phone).
- The person making a Multic is a **creator**. The person playing one is a
  **reader** (solo) or a **player** (when it's interactive or multiplayer).

Hold this line everywhere. The noun is the brand.

---

## Voice: precise, clear, with measured play

Three principles, in priority order. When they conflict, the higher one wins.

### 1. Clarity first
Every sentence earns its place. One idea per sentence. The reader always knows
what to do next. If a paragraph doesn't help the reader act or understand, cut
it.

### 2. Precise, never stiff
Concrete nouns, real verbs, exact names. Use the product's own terms (**Frame**,
**Choice**, **QTE**, **Design Canvas**) rather than vague paraphrases. No hype,
no filler, no hedging.

### 3. Play with intent
A light touch of personality — at the **edges**, never in the load-bearing
middle. Play serves momentum and warmth; it never serves the writer's amusement.
A reader who is stuck or paying us money should never have to wade through a joke
to find the answer.

---

## Where play is allowed (and where it is banned)

| Allowed — bring warmth here | Banned — keep it clean here |
| --- | --- |
| Page and section openers | Numbered steps / procedures |
| Transitions between ideas | Reference tables (nodes, models, credits) |
| Empty states, success moments | Warnings, errors, billing, limits |
| The occasional one-line aside | Anything a frustrated reader reads when stuck |

**Rule of thumb:** if the reader might be confused, scared, or out of credits,
write it straight.

---

## Register map (match the tone to the page)

- **Concept / "what is" / overview pages** — warmest. A little evocative. This is
  where a creator falls in love with the idea. Play allowed.
- **How-to / step-by-step** — calm, precise, imperative. Lead with the action.
  Minimal play.
- **Reference (nodes, models, credits, API)** — terse and scannable. Zero play.
- **Microcopy (empty/success/error states)** — this is where a *little* play pays
  off most. One human line beats three neutral ones.

---

## Mechanics

- **Second person, active voice, present tense.** "You publish a Multic", not
  "Multics can be published".
- **Sentence case headings.** "Publish your first Multic", not "Publish Your
  First Multic".
- **Bold for UI elements:** Open **Manage**, then select **Publish**.
- **Code formatting** for filenames, paths, values, and node/field names in
  reference context: `docs.json`, `frame.aspectRatio`.
- **Short paragraphs.** Lead with the point; support it after. Never bury the
  action in the third sentence.
- **One exclamation mark per page, maximum.** Usually zero.
- Oxford comma. Em dashes sparingly. No emoji in body copy (sidebar icons are
  fine).

---

## Words we use — and don't

**Use:** make, create, generate (art), wire (a branch), publish, play, read,
together, creator, reader, player, Multic, credits.

**Avoid:**
- "user" when you mean *creator* or *reader* — name who it is.
- "content", "asset" in reader-facing copy (fine in Studio/reference context).
- "watch" for playing a Multic — they *play* or *read* it; it's interactive.
- Hype words: "powerful", "seamless", "magic", "revolutionary", "effortless".
- Crutch words: "simply", "just", "easily" — if it were simple we wouldn't be
  documenting it.

---

## Worked examples

**Concept opener — warmth allowed**
- ✅ "Every Multic starts with a frame and a question: what happens next?"
- ❌ "Multic is a powerful platform that empowers creators to easily build
  engaging interactive content."

**How-to — straight, no play**
- ✅ "Open **Manage**, add cover art and a tagline, then select **Publish**.
  Your Multic appears in the feed within a minute."
- ❌ "Time for the fun part — let's get this baby out into the world! Smash that
  **Publish** button and watch the magic happen."

**Reference — terse, scannable**
- ✅ "**Choice** — a branching point. Each option routes to a different node.
  Up to six options per Choice."
- ❌ "The Choice node is a really versatile tool that lets you create all sorts
  of exciting branching possibilities for your players to enjoy."

---

## How this stays handcrafted even when machines help

Docs are tiered. Voice-bearing pages are written or edited by a human (or an
agent held to this guide); only mechanical content auto-commits.

| Tier | Examples | Pipeline |
| --- | --- | --- |
| **Generated** | Changelog (from commits), node/API reference (from `story-core` types), model & credit tables (from `ai-models-config`) | Bot → `dev` → may auto-merge |
| **Assisted** | Feature pages when behaviour changes | Agent opens a **draft PR** on `dev`; a human edits for voice and merges |
| **Handcrafted** | Concept, getting-started, anything voice-bearing | Human/agent author; review required |

Guardrails:
1. **This file is canon.** `AGENTS.md` points every agent here.
2. **Golden pages** (see `getting-started/what-is-a-multic.mdx`) are the worked
   bar new pages are compared against.
3. **A voice-lint review** runs on every docs PR — it scores changed `.mdx`
   against this guide and the golden pages and flags off-voice prose before a
   human approves.
4. **No bot writes to `main`.** Drafts land as PRs on `dev`; the preview URL and
   a human are the gate.
