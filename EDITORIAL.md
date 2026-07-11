# Public documentation lifecycle

This repository publishes reader-facing Multic documentation. It works with the
private knowledge site, but it does not inherit private material by default.

## Page lifecycle

| Status | Meaning | Allowed branch |
| --- | --- | --- |
| `draft` | Early work; claims may be incomplete | `dev` |
| `pending_human_review` | Ready for Jake to review; not public truth | `dev` |
| `approved` | Current evidence checked and Jake approved the wording | `main` and `dev` |
| `stale` | The review trigger passed or evidence changed | `dev`; remove from `main` navigation if materially unsafe |
| `retired` | The product behaviour or reader need no longer exists | Git history; redirect when a public URL existed |

Delete abandoned drafts and superseded template material. Git history is the
archive. Preserve a retired page only when its history, redirect, or migration
path still helps readers.

## Review packet

Each request in `#docs-validation` should contain:

1. clickable preview links and the exact pages changed;
2. a one-sentence description of the reader outcome;
3. the product evidence used and the date it was checked;
4. unresolved product or tone questions;
5. the human and agent contributions recorded in metadata;
6. whether the change is safe to promote to `main`.

Jake's approval moves a page to `approved`, sets `last_verified` and
`review_after`, and resolves `tone_review`. Substantive later edits return it to
`pending_human_review` unless they are generated from an already approved
contract.

## Public/private mirror contract

The private knowledge site has two distinct, read-only feeds:

- `public-approved` mirrors `main` and represents current approved public truth.
- `public-preview` may mirror `dev`, but must remain unmistakably labelled as a
  draft source.

Every mirrored page records repository, path, Git ref, commit SHA, and sync
timestamp. Private notes can link to or annotate a mirror without editing it.

A private draft can carry `public_candidate`, but publication is a separate
workflow. It must be copied into this repository, checked against the current
product, reviewed in `#docs-validation`, and approved by Jake before reaching
`main`.

## Authorship convention

The frontmatter record describes contributions, not prestige:

```yaml
authorship:
  human:
    - name: Jake Dickson
      role: product direction and human review
  agents:
    - name: OpenAI Codex
      role: research, structure, and editorial draft
```

Use an empty list when a category did not contribute. Generated reference pages
also record their generator and authoritative source. Public presentation can be
compact; the repository record remains explicit.

## Review cadence

Set cadence by risk:

- 30 days: pricing, credits, availability, limits, integrations, and live UI
  procedures;
- 90 days: feature concepts and workflows;
- 180 days: stable mental models and editorial guidance.

Review sooner when the product, terminology, or evidence changes. Cadence is a
triage mechanism, not a promise that unchecked prose stays true until its date.
