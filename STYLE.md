# Multic documentation — evolving editorial guide

This is the current working guide for public Multic documentation. It is a
review rubric, not a constitution. Product evidence, reader comprehension, and
good editorial judgment can change it.

When you improve the voice or vocabulary, update this guide and the affected
pages together. Record the change in the validation note so Jake can judge the
direction rather than silently inheriting it.

## The current one-line description

Multic is where you **make and play interactive comics** — branching, animated,
voiced, and playable with friends.

That sentence is a working description, not a promise that every capability is
available in every product surface. Verify feature-level claims before
publication.

## Working vocabulary

- The thing a creator makes is **a Multic**: capitalised and countable.
- Creators make Multics in **Studio**.
- A **reader** reads a solo Multic; a **player** takes part when interaction or
  multiplayer is relevant.
- Current mechanic names include **Frame**, **Dialogue**, **Narration**,
  **Choice**, and **QTE**.

Prefer the product's real labels over this list. When the interface and the
guide disagree, flag the mismatch and decide which one should change.

## Voice: intelligent, authoritative, open-minded

The docs should know what they know, say what they do not, and help the reader
move. Three principles guide the voice.

### Clarity first

Every sentence earns its place. Lead with the answer or action. Keep one main
idea in each paragraph. If a detail neither helps a reader act nor builds the
right mental model, cut it.

### Precise without becoming stiff

Use concrete nouns, active verbs, exact UI labels, and real constraints. Prefer
**Choice** to “interactive element” when Choice is what you mean. State
uncertainty plainly rather than laundering it into confident prose.

### Play with intent

A little personality belongs at the edges: openers, transitions, empty states,
and moments of success. Never put the joke between a stuck reader and the fix.

| More warmth is useful | Keep it straight |
| --- | --- |
| Concept and overview pages | Procedures and prerequisites |
| Transitions and success moments | Warnings, errors, limits, and billing |
| Carefully chosen asides | Reference tables and exact values |

## Match the register to the job

- **Concept and overview:** warm, vivid, and concise. Build the mental model.
- **How-to:** calm, direct, and imperative. Make the next action obvious.
- **Reference:** terse and scannable. Remove personality that competes with
  exactness.
- **Troubleshooting:** empathetic but unsentimental. Diagnose first, then fix.
- **Microcopy:** human and brief. One useful line beats three neutral ones.

## Mechanics

- Use second person, active voice, and present tense.
- Use sentence case for headings.
- Bold interface labels: Open **Manage**, then select **Publish**.
- Use code formatting for filenames, paths, values, and fields.
- Keep paragraphs short and make links descriptive out of context.
- Use Oxford commas. Use em dashes and exclamation marks sparingly.
- Do not use emoji as decoration in body copy.
- Give images and media useful alt text. Do not encode meaning in colour alone.

## Words that usually help

Prefer: make, create, generate (art), connect, branch, publish, play, read,
together, creator, reader, player, Multic.

Be suspicious of:

- “user” when creator, reader, or player is more exact;
- “content” or “asset” in reader-facing prose when a concrete noun exists;
- “watch” when the Multic asks someone to act;
- hype such as “powerful”, “seamless”, “magic”, or “revolutionary”;
- crutches such as “simply”, “just”, and “easily”;
- generic conclusions that repeat the page without helping the reader continue.

These are editorial prompts, not banned-word theatre. Use a suspicious word when
it is the clearest accurate word, then be ready to explain why.

## A small worked bar

**Concept opener**

- Better: “Every Multic starts with a frame and a question: what happens next?”
- Worse: “Multic is a powerful platform for seamless interactive content.”

**Procedure**

- Better: “Open **Manage**, add cover art and a tagline, then select
  **Publish**.”
- Worse: “Time for the fun part — smash that button and watch the magic happen.”

**Reference**

- Better: “**Choice** — a branching point. Each option routes to another node.”
- Worse: “The Choice node lets you create all sorts of exciting possibilities.”

The better examples demonstrate shape and restraint. They are not approved
product claims until verified.

## Human authorship and agent assistance

Public documentation should retain human judgment without pretending agents did
not contribute.

- Voice-bearing pages need meaningful human direction or editing, a visible
  human editorial owner, and explicit approval before production.
- Agent-written or agent-revised material names the agent and its role in page
  metadata.
- Mechanical reference generation identifies its source and generator.
- Approval alone is recorded as review, not retroactively relabelled as writing.
- A compact public byline may omit process detail, but repository metadata keeps
  the full provenance.

Jake Dickson is the current human reviewer. A page can live on `dev` while his
review is pending; it cannot become approved public truth on `main` without that
review.

## Currentness is part of the prose

Every page has a status, confidence, last-updated date, evidence-backed
last-verified date, and review trigger. A passed review date creates work. It
does not make the page silently disappear or claim that the content is wrong.

When a claim is uncertain, say so in the draft and take it to validation. Do not
fill a blank with plausible product fiction.

## How this guide evolves

During review, ask:

1. Is the page accurate today?
2. Can the intended reader act or build the right mental model?
3. Does it sound like an intelligent person rather than a template?
4. Is the confidence proportional to the evidence?
5. Does the authorship record match the work?
6. Should this page change the guide?

Tone review is a named metadata state: `pending`, `accepted`, or
`needs_revision`. It belongs beside product verification rather than masquerading
as automated truth.
