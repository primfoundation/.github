# Prim Foundation repository lifecycle

Repositories are organized by **independent responsibility**, not by file type, route, temporary experiment, or a desire to minimize repo count.

## Lifecycle states

| State | Meaning |
| --- | --- |
| `active` | Canonical home for an independent standard/platform/product responsibility. |
| `incubating` | An experiment discovering a contract/product; may later merge, split, or retire. |
| `migrating` | Successor selected and compatibility work in progress. No new unrelated scope. |
| `compatibility` | Read-only or narrowly maintained legacy surface kept for consumers/migrations. |
| `archived` | Historical record; no longer authoritative. Successor and last supported state are documented. |

Archival is not deletion.

## Repository creation test

Create a new top-level repository only when all are true:

1. the responsibility is coherent and nameable;
2. it has a materially independent release/security/runtime lifecycle;
3. it cannot reasonably be a profile/package/app within an existing responsibility;
4. ownership and maintenance expectations are explicit;
5. the new boundary reduces coupling rather than merely moving files.

A new Prim profile, Cloudflare route, viewer, migration utility or experimental schema does not automatically pass this test.

## Migration/rename gate

Before renaming or consolidating a repository:

- inventory default/open branches, PRs/issues, releases/packages, domains/deployments, dependency references and secret **names**;
- record the exact source commit(s) being migrated;
- identify runtime identities whose stability matters independently from the repo slug;
- preserve Git provenance/history or document an explicit imported lineage;
- move tests/contracts before traffic/consumer cutover;
- supply compatibility redirects/aliases/read-old behavior where required;
- prove a clean clone/build/test of the successor;
- retain rollback.

## Archive completion contract

A repository may be archived only when:

- its responsibility has a named successor or an explicit recorded reason for termination;
- relevant open PRs/issues have been migrated, completed, or deliberately closed with preserved rationale;
- consumers and production routes have moved or intentionally remain on a compatibility surface;
- tests and real-use verification pass on the successor;
- rollback window has elapsed or a retained compatibility path makes rollback unnecessary;
- README points to successor, source lineage and last supported release/commit;
- private/security/history review permits the chosen visibility and archive action.

Never force-push/delete history as routine cleanup. Never change semantic profile identity solely because its repository changed.
