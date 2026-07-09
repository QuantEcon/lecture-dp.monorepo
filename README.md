# lecture-dp.monorepo — disposable test double

> **This is not a real lecture repository.** It is a temporary, disposable
> **test double** of [QuantEcon/lecture-dp](https://github.com/QuantEcon/lecture-dp),
> used to develop and exercise the sync / promotion / drift-detection machinery
> of [QuantEcon/lectures](https://github.com/QuantEcon/lectures) without touching
> any live lecture repository.

The authoritative *Dynamic Programming* lectures live in
[QuantEcon/lecture-dp](https://github.com/QuantEcon/lecture-dp) and are published from there.
Nothing in this repository is published anywhere.

## What this repo is for

The `QuantEcon/lectures` monorepo keeps every live lecture repository strictly
**read-only** while its tooling is developed. But proving that tooling works
requires *making* upstream edits — for example, deliberately editing a lecture
here to confirm the monorepo's drift-check raises an alarm. This repository
exists so those edits have somewhere safe to happen.

- Seeded **tree-only** (no history) from `QuantEcon/lecture-dp@0a12f79c`:
  `lectures/` and `environment.yml`, nothing else.
- Consumed by the `dp-test` entry in the monorepo's `sync/manifest.yml`.
- Edits made here are deliberate test fixtures, not content improvements.

## Lifecycle

Created 2026-07-09 for the monorepo's M2 development phase. When the dp pilot
(M3) switches over to the real `lecture-dp`, this repository will be archived
or deleted.
