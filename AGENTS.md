# Public documentation project instructions

## What this repository is

- This is the public documentation source for **Multic**, built with
  [Mintlify](https://mintlify.com).
- Pages are MDX with YAML frontmatter. Site configuration lives in `docs.json`.
- This repository must not contain internal architecture, operations,
  financials, unreleased plans, private research, or personal notes.
- The separate private knowledge repository may mirror approved public pages.
  Private material never flows back here without deliberate editorial review.

## Environments and branches

- `dev` is the working preview. Drafts and unverified pages belong here.
- `main` is the production source for approved public documentation.
- Nothing reaches `main` until Jake Dickson approves the affected pages. Surface
  preview links and a concise page list in `#docs-validation` for that review.
- Public docs are pre-launch. Keep the site `noindex` until Jake explicitly
  approves publication and the production domain is ready.

## Start with evidence

Before documenting behaviour, inspect the current product or its source. Link
the evidence in the pull request or validation message. Do not turn a roadmap,
plan, old screenshot, or another doc into a product claim without checking it.

When evidence conflicts with a page, the evidence wins. Update the page and its
currentness metadata in the same change.

## Voice and vocabulary

Read `STYLE.md` before writing. It is an evolving editorial guide, not immutable
canon. Use it as the current working bar, then raise questions when the product,
audience, or a better sentence calls for a change.

Current preferred terms include **a Multic**, **Studio**, creator, reader, and
player. Treat those terms as deliberate defaults rather than laws. If the live
product uses different language, flag the mismatch and resolve it instead of
papering over it.

## Required page metadata

Every public MDX page carries custom metadata in addition to `title` and
`description`:

```yaml
knowledge_id: public.area.page-name
status: pending_human_review
confidence: medium
owner: Jake Dickson
last_updated: "YYYY-MM-DD"
last_verified: null
review_after: null
tone_review: pending
authorship:
  human:
    - name: Jake Dickson
      role: product direction
  agents:
    - name: OpenAI Codex
      role: editorial draft
```

Use a stable `knowledge_id`; do not change it when a file moves. Allowed status
values are `draft`, `pending_human_review`, `approved`, `stale`, and `retired`.
Allowed confidence values are `low`, `medium`, and `high`.

`last_verified` means the product claim was checked against current evidence on
that date. Leave it `null` when it was not checked. `review_after` is a review
trigger, not an expiry date: passing it makes a page due for review, not
automatically false.

Authorship must describe what happened. Name meaningful human direction,
writing, editing, and approval. Name material agent assistance and its role. Do
not manufacture a human byline for an agent-written draft, and do not erase the
human behind the product direction.

See `EDITORIAL.md` for the lifecycle, approval, and mirroring contract.

## Workflow

1. Read `docs.json`, `STYLE.md`, `EDITORIAL.md`, and nearby pages.
2. Establish current evidence for every behavioural claim.
3. Write the smallest page that solves the reader's problem. Mark uncertainty
   with an MDX TODO comment rather than guessing.
4. Update navigation and metadata together.
5. Run `mint validate`, `mint broken-links`, and `mint a11y`.
6. Report changed pages, evidence, unresolved questions, and preview links in
   `#docs-validation`.
7. Jake approves the public wording before it enters `main`.

For current Mintlify components and configuration, use the official Mintlify
documentation skill (`npx skills add https://mintlify.com/docs`).
