# Prim Foundation security policy

Prim software frequently handles local files, credentials, browser sessions, personal records, and untrusted definition/content inputs. Treat those boundaries as security-relevant even when a repository looks like a small utility.

## Reporting a vulnerability

Prefer the affected repository's **private vulnerability reporting / security advisory** channel when GitHub exposes it. If the repository has a more specific `SECURITY.md`, that policy wins.

If no private channel is available, do **not** post exploit details, credentials, private Prim contents, or personal data in a public issue. Open a minimal public issue asking a maintainer for a private reporting channel and include no sensitive technical detail.

## Default boundaries

Unless a repository explicitly and safely documents otherwise:

- Prim definitions are untrusted data and do not gain code-execution authority merely by being discoverable or valid.
- A structurally valid Prim is not thereby factual, safe, authorized, reviewed, or publisher-authenticated.
- Public Foundation services distribute public definitions/metadata; they do not require private user Prim contents.
- Secrets belong in platform/keychain/secret-manager bindings, never repository source, fixtures, logs, screenshots, telemetry, or generated roadmaps.
- Renderers must treat pack content as hostile input; HTML/script/URL/archive/parser boundaries need explicit tests.
- A product rename never silently rotates bundle identifiers, Keychain services, data roots, cookie/session contracts, file encodings, signing identities, or public API identities.
- Repository/profile source relocation does not silently change semantic identity.

## Release claims

Keep these states separate in security and release communication:

`implemented` → `tested` → `reviewed` → `released` → `deployed` → `verified in real use`.

A passing CI run does not establish independent security review, production safety, factual truth, privacy compliance, or real-user acceptance.

## Sensitive migrations

Before a public/private visibility change, repository consolidation, account migration, profile import, or archive:

1. inspect current and historical content for secrets/private data;
2. identify consumers and compatibility-sensitive identifiers;
3. preserve provenance and rollback;
4. migrate tests before production traffic;
5. verify the replacement in real use;
6. retain the old history read-only when archival is appropriate.

Never rewrite/delete history merely to make an organization diagram look clean. If history contains material that must be removed for legal/security reasons, treat that as a separate reviewed incident response.
