# consensus-persona-respawn

Lifecycle management for consensus personas.

`consensus-persona-respawn` replaces dead or degraded personas with ledger-informed successors, preserving governance continuity while adapting to failure patterns.

## Why it matters

Static persona sets decay over time. Respawn keeps your decision system healthy by evolving weak performers instead of letting governance quality drift.

## Core capabilities

- strict schema validation
- idempotent respawn decisions
- lineage-aware persona replacement
- board-native artifact writes for audit and replay

## Best use cases

- long-running guard systems
- recurring policy domains with drift
- governance loops that require explicit adaptation history

## Quick start

```bash
npm i
node --import tsx run.js --input ./examples/input.json
```

## Test

```bash
npm test
```

## Continuous improvement

See `AI-SELF-IMPROVEMENT.md` for how to tune respawn heuristics safely.
