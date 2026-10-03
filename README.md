# ATLAS Starter Vault

**Version 0.1 — Working / Starter Architecture**

An [Obsidian](https://obsidian.md) vault scaffold for **ATLAS**, the structured memory / knowledge layer within the broader **LIOS** architecture. It is a starting point for continued architectural development, not a finished implementation.

> **Storage does not equal trust.**

## What this is

ATLAS preserves what happened, what was learned from it, what became trusted knowledge, what became capability, and what governance authorized, without letting those states collapse into one another.

```
Experience → Learning → Knowledge → Capability → Authorized Behavior
```

Each arrow is a promotion that must be earned, never assumed:

| Distinction | Meaning |
|---|---|
| Experience ≠ Learning | An observation can exist without a valid interpretation. |
| Learning ≠ Knowledge | A hypothesis can be useful without being sufficiently validated. |
| Knowledge ≠ Capability | Knowing something doesn't mean the system can operationalize it. |
| Capability ≠ Authorization | Being able to do something isn't permission to do it. |

## Status: intentionally incomplete

Many questions are deliberately **OPEN**, and this vault does not invent answers to them. This includes promotion rules, evidence thresholds, the uncertainty model, contradiction and supersession mechanics, authority and distributed governance, the LIOS ↔ ATLAS ↔ STAIR-G interfaces, the Hermes mapping, and the Hub vs. Living Hub terminology.

- Open questions: [Open Decisions](91%20-%20Governance/Open%20Decisions.md)
- Settled items: [Resolved Decisions](97%20-%20Decisions/Resolved%20Decisions.md)
- Central open thread: [Experience Boundary](00%20-%20ATLAS/Experience%20Boundary.md)

## Getting started

1. Clone or download this repo.
2. In Obsidian: **Open folder as vault** and select the repo folder.
3. Start with [ATLAS Overview](00%20-%20ATLAS/ATLAS%20Overview.md) and [ATLAS Index](99%20-%20Index/ATLAS%20Index.md).
4. To add an item, copy the matching file from `90 - Templates/` into its numbered folder.

Notes are linked with Obsidian wikilinks (`[[Note Name]]`), which GitHub does not render as links. Browse in Obsidian for the full link graph.

## Structure

| Folder | Contents |
|---|---|
| `00 - ATLAS` | Overview, ontology, Experience boundary |
| `01 - Experience` … `05 - Authorized Behavior` | One folder per stage of the epistemic progression |
| `06 - Entities` | Nodes, actors, authorities (Node ≠ device) |
| `07 - Relationships` | Typed links between items |
| `08 - Ledger` | Ledger events |
| `09 - Actions & Feedback` | Actions taken and feedback received |
| `90 - Templates` | Frontmatter + body templates |
| `91 - Governance` | Open decisions, promotion rules |
| `92 - LINT` | ATLAS LINT spec |
| `93 - STAIR-G` | STAIR-G interface |
| `94 - LIOS` | LIOS interface |
| `95 - Hermes` | Hermes interface (mapping OPEN) |
| `96 - Architecture` | Current architecture |
| `97 - Decisions` | Resolved decisions |
| `98 - Registers` | Change log |
| `99 - Index` | Index |

## Architecture at a glance

```
EXPERIENCE → ATLAS (memory/state) → ATLAS LINT (integrity)
  → STAIR-G (evaluate/learn/propose/validate)
  → AUTHORITY / GOVERNANCE → CAPABILITY / AUTHORIZATION
  → ACTION / OUTCOME → back to EXPERIENCE
```

- **ATLAS**: durable epistemic state and provenance.
- **ATLAS LINT**: inspects *existing* ATLAS only. It auto-fixes deterministic issues (then verifies and logs) and flags interpretive ones for human review. It never creates Knowledge, promotes Learning, authorizes Capability, resolves substantive disagreement, or changes governance.
- **STAIR-G**: governed improvement loop. It never lets Experience automatically become trusted Capability.
- **LIOS**: the overarching capability/governance architecture.
- **Hermes**: an implementation pattern; it must not reshape the LIOS / STAIR-G boundaries.

See [Current Architecture](96%20-%20Architecture/Current%20Architecture.md).

## Invariants

1. Experience is evidence; interpretation may evolve.
2. Learning is not automatically Knowledge.
3. Knowledge is not automatically Capability.
4. Capability is not automatically Authorization.
5. Storage does not equal trust.
6. No experience should automatically become trusted capability.
7. Historical provenance stays traceable.
8. Contradiction is represented, never silently erased. Superseded items are kept.
9. Governance can adapt when capability changes.

## Conventions

- Every item carries YAML frontmatter (`type`, `status`, `id`, provenance fields).
- Statuses in the ontology are *candidates*, not a finalized state model.
- Don't rewrite historical Knowledge; supersede it and record the relationship.
- When a decision is made, move it from Open Decisions to Resolved Decisions and note it in the [Change Log](98%20-%20Registers/Change%20Log.md).
- Where something is OPEN, add a clearly labeled open thread rather than a guess.

## Known provisional pieces

- `90 - Templates/ATLAS Item.md` was listed in the build spec without contents; its fields are a minimal skeleton.
- `07 - Relationships` and `09 - Actions & Feedback` have no templates yet; whether these are separate file types is an open ontology question.

## License

Not yet specified.
