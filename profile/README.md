<div align="center">

# Prim

**A file that stores information, and tools that interact with it.**

[prims.sh](https://prims.sh) · [Specification](https://github.com/primfoundation/prim/blob/main/SPEC.md) · [What is a Prim?](https://github.com/primfoundation/prim/blob/main/WHAT-IS-PRIM.md) · MIT

</div>

---

## The problem

Knowledge work runs on formats designed before agents existed. Spreadsheets hold structure, documents hold decisions, decks hold the story, notes hold memory — and every one of them was built for one person at one machine. Hand those to an agent and you get scraping, guessing which tab is authoritative, and claims that carry no evidence.

Today an agent does real work and then flattens it into an `.xlsx` or a chat log. The next agent has to reverse-engineer it. The work dies when the window closes.

## The inversion

**Store the concept. Generate the files.**

A Prim is a self-contained pack of knowledge. The Prim is the source of truth; the spreadsheet, the document, and the deck are projections rendered out of it.

| Property | What it means |
|---|---|
| **AI-native** | Agents read, validate, and reason over the pack directly — no translation layer |
| **Evidence-first** | Claims carry provenance, trust tiers, and hashes; validation is fail-closed |
| **Durable** | Versioned, supersedable memory that outlives the session, the agent, and the vendor |
| **Human-inspectable** | Still openable and understandable by a person |
| **No fixed UX** | Views are rendered on demand; a Prim Tool operates on the pack |
| **Portable** | One file moves desk to desk, agent to agent — *"send me the prim"* |

## Packaging

| Form | Role |
|---|---|
| Directory pack | Canonical source of truth — git, editing, validation |
| `.prim.zip` | Primary interchange. Attach this when someone says *send me the prim* |
| `.prim.tar.gz` | Allowed. Unix and agent workflows |
| `.prim` | Reserved branded container (zip under the hood) |

## Repositories

| Repo | What it is |
|---|---|
| **[prim](https://github.com/primfoundation/prim)** | Category home — specification, family map, registry, TypeScript SDK, viewer |
| **[prim.workbook](https://github.com/primfoundation/prim.workbook)** | Worksheets composing expected + actuals, citing measure/metric |

Domain profiles (`prim.emf`, `prim.orf`, `prim.ocsf`, `prim.osf` and others) are catalogued in [FAMILY.md](https://github.com/primfoundation/prim/blob/main/FAMILY.md).

## Status

**Early, and honest about it.** The category specification is at `v0.4.0-draft`. Profiles are being written, the registry is small, and the tooling is thin. The spec, the family map, and the packaging rules are all in the open under MIT so they can be argued with.

If you are evaluating this: start with [WHAT-IS-PRIM.md](https://github.com/primfoundation/prim/blob/main/WHAT-IS-PRIM.md), then read [SPEC.md](https://github.com/primfoundation/prim/blob/main/SPEC.md), then open [`examples/minimal-concept`](https://github.com/primfoundation/prim/tree/main/examples/minimal-concept).

## How to say it

> "Send me the prim."
>
> "Don't send the spreadsheet — just send the prim."
>
> "The prim is the source of truth. The deck is just a view."

---

<div align="center">
<sub>Prim Foundation · MIT licensed · <a href="https://prims.sh">prims.sh</a></sub>
</div>
