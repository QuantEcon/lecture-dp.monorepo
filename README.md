# lecture-dp.monorepo — disposable test double

> **This is not a real lecture repository.** It is a temporary, disposable
> **test double** of [QuantEcon/lecture-dp](https://github.com/QuantEcon/lecture-dp):
> the one lecture repository the [QuantEcon/lectures](https://github.com/QuantEcon/lectures)
> monorepo may write to before its cutover, so that no live one is touched.

The authoritative *Dynamic Programming* lectures live in
[QuantEcon/lecture-dp](https://github.com/QuantEcon/lecture-dp) and are published from there.
Nothing in this repository is published anywhere.

## What this repo is for

The `QuantEcon/lectures` monorepo keeps every live lecture repository strictly
**read-only** until its cutover. But proving its tooling works requires
*writing* to a lecture repository. This repository exists so those writes have
somewhere safe to happen.

- Seeded **tree-only** (no history) from `QuantEcon/lecture-dp@0a12f79c`:
  `lectures/` and `environment.yml`, nothing else.
- **First, a sync source.** The `dp-test` entry in the monorepo's
  `sync/manifest.yml` read this repository in `lecture-dp`'s place, and edits
  made here were deliberate test fixtures for the drift-check, not content
  improvements. That entry was removed on 2026-11-03 (QuantEcon/lectures#33,
  step 1 of QuantEcon/project-monorepo#24): the monorepo reads the real
  `lecture-dp`, and nothing here feeds its pool.
- **Now, the rehearsal target.** The publishing rehearsal
  (QuantEcon/project-monorepo#27) releases, deploys and rolls back the
  monorepo's builds here: it is the only place the monorepo may freely push
  built HTML before a cutover.

## Lifecycle

Created 2026-07-09 for the monorepo's M2 development phase. Its role as a sync
source ended on 2026-11-03, when the monorepo switched to the real
`lecture-dp`. The repository stays as the rehearsal target, and is retired by
the cutover of `dp` (QuantEcon/project-monorepo#85), not before.
