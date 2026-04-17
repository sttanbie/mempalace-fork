# mempalace-fork (sttanbie)

Fork of [MemPalace/mempalace](https://github.com/MemPalace/mempalace) for the Sttan ecosystem.

## Why this fork exists

Risk mitigation for the Sttan AIOS ecosystem. MemPalace is the memory backend
powering `memory_layer` (see: [EPIC-MPL-001](https://github.com/sttanbie/mempalace-fork)).

This fork exists as a **safety net** — not because there are problems upstream.
MemPalace upstream is healthy (47k+ stars, active daily). If upstream introduces
a breaking change or goes dormant, we can patch here without emergency work.

## Branch policy

| Branch | Purpose |
|--------|---------|
| `main` | Mirror of upstream MemPalace/mempalace main |
| `sttan-main` | Sttan ecosystem customizations (pinned version, local patches) |

## How to sync with upstream

```bash
git remote add upstream https://github.com/MemPalace/mempalace.git
git fetch upstream
git checkout sttan-main
git merge upstream/main
git push origin sttan-main
```

Sync quarterly or when upstream releases a version we need.

## Contribution policy

Bugs that affect upstream should be reported and PRed to MemPalace/mempalace first.
Only patches that are Sttan-specific or time-sensitive go into `sttan-main`.
