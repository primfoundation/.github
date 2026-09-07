<div align="center">

# Prim Foundation

**Store the concept. Generate the files.**

[prims.sh](https://prims.sh) · [Prim specification](https://github.com/primfoundation/prim) · MIT

</div>

---

Knowledge work should survive the app, agent, employee, model vendor, and session that happened to create it.

A **Prim** is a durable, portable information/work-product record. The Prim is the source of truth; spreadsheets, documents, decks, dashboards, and other interfaces are views or projections when that model fits the domain.

## Design commitments

| Commitment | Meaning |
| --- | --- |
| **Durable** | Important state survives sessions and replaceable intelligence. |
| **AI-native** | Agents can inspect and operate the structured record directly instead of reverse-engineering a human-only export. |
| **Human-inspectable** | A person can understand the record and its important provenance without trusting a black box. |
| **Portable** | Semantic identity and useful operation do not depend on one repository, hosted account, model vendor, or UI. |
| **Evidence-aware** | Profiles can preserve sources, observations, claims and provenance without treating a citation/hash/validator pass as truth. |
| **Tool-independent** | Prim Tools, agents and renderers operate on the record; they are not the durable record itself. |

A simple Prim should stay simple. The Foundation does not require every record to become a universal knowledge graph, enterprise workflow, or giant taxonomy.

## Foundation architecture

**`primfoundation/prim`** is the standards/profile/conformance home. Foundation-maintained profiles can coexist as portable packages; a new profile does not require a new repository.

**`prims.sh`** is the public discovery/distribution surface: humans and agents can find definitions, inspect exact versions, and use the public API/MCP. Public Foundation infrastructure distributes definitions and public metadata—it does not need to store users' private Prim instances.

Independent products have their own release/security lifecycles while consuming the same portable contracts:

- **Prims Desktop** — generic desktop host/inspector.
- **Primboard** — private encrypted spatial intake board for material that may later become a Prim or task.
- **Prims Browsers** — sandbox browsers agents can drive without taking over the user's local pointer/session.

The organization is actively consolidating historical experiments around these responsibility boundaries. Old repositories are preserved as compatibility/history until their responsibilities have verifiably moved; they are not deleted to make the diagram prettier.

## Definitions, tools, and trust

A profile definition says how a kind of durable record is represented/checked. A Prim Tool opens, edits, renders, connects, imports, exports, or otherwise operates on Prims.

Keep these judgments separate:

**official** ≠ **popular** ≠ **conformant** ≠ **security-reviewed** ≠ **factually true**.

Likewise, a record describing a capability does not grant that capability, and a writable label saying “approved by a human” is not authentication by itself.

## Status

Early and intentionally explicit about it. The category/profile architecture, compatibility work, Foundation Library/MCP, Cloudflare Hub migration, Research vNext, and reference products are under active development. Passing tests are retained as evidence of tested scope; they are not presented as proof that every migration, security review, deployment, or real-user gate is complete.

Start with [the Prim repository](https://github.com/primfoundation/prim) and [prims.sh](https://prims.sh).

---

<div align="center">
<sub>Prim Foundation · open standards and reference tools · <a href="https://prims.sh">prims.sh</a></sub>
</div>
