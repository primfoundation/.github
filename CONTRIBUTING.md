# Contributing to Prim Foundation projects

Thank you for helping build durable work products that humans and agents can both use.

A repository-specific `CONTRIBUTING.md` overrides this default when it defines a narrower build/release process.

## Start with the ownership boundary

Before changing code or formats, identify what the repository owns:

- **`prim` / definitions:** semantic contracts, profile packaging, compatibility and conformance.
- **Foundation Hub:** public discovery, distribution, API/MCP, ranking and platform operations—not users' private Prim instances.
- **Products:** their own UI/runtime/security behavior while consuming portable Prim contracts.

Do not move domain semantics into a UI merely because it is convenient, and do not move product-specific orchestration into a universal profile without evidence it generalizes.

## Change discipline

- Preserve existing data and compatibility unless a versioned migration explicitly says otherwise.
- A file/repository move does not change profile identity.
- A user-facing rename does not imply a runtime identifier migration.
- Prefer additive, reversible changes over flag-day rewrites.
- Keep source artifacts/evidence distinct from claims about the things they describe.
- Preserve unknown fields when forward-compatible interchange is intended.
- Never silently promote inferred/predicted/hypothetical content into stated/observed fact.
- Do not make validity, popularity, official status, security review, publisher identity, and factual truth interchangeable labels.

## Tests and evidence

A useful PR states:

1. the user/system outcome;
2. the compatibility/security boundaries touched;
3. exact tests run and where;
4. what was **not** tested;
5. whether anything was released/deployed/verified with real users.

New format rules need positive and negative fixtures. Migration code needs original fixtures, loss behavior and rollback. Platform changes need health/rollback evidence. Native macOS/TCC/signing changes need a real-Mac gate when CI cannot prove the behavior.

## Privacy and secrets

Never commit private Prim instances, production credentials, API keys, OAuth private keys, personal records, customer data, private browser cookies, or secret values. Use fictional/minimized fixtures. When importing historical work, inspect source history and visibility before making anything public.

## Repository lifecycle

Do not create a repository just because a new Prim type or route exists. Prefer the existing standards/profile package model or the existing product/control-plane repo. A new repository is justified by a materially independent product/release/security/runtime lifecycle.

Do not archive/delete a repository until its successor, compatibility, rollback, consumer migration and real-use proof are recorded.
