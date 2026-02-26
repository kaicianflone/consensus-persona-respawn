---
name: consensus-persona-respawn
description: Ledger-informed persona lifecycle management. Replaces low-performing personas with successor personas derived from mistake patterns in board decision history, preserving adaptive governance over long-running automation.
homepage: https://github.com/kaicianflone/consensus-persona-respawn
source: https://github.com/kaicianflone/consensus-persona-respawn
---

# consensus-persona-respawn

`consensus-persona-respawn` is the adaptive maintenance loop for persona governance.

## What this skill does

- identifies dead/weak personas by trigger or reputation threshold
- mines historical decision artifacts for mistake patterns
- generates successor persona profiles informed by those failures
- writes `persona_respawn` and updated `persona_set` artifacts
- keeps governance panel quality from stagnating

## Why this matters

A static evaluator panel drifts over time. This skill provides lifecycle renewal so consensus quality improves instead of degrading.

## Ecosystem role

Extends persona-generator with long-term adaptation and ties directly into board-ledger evidence.

## Best use cases

- long-running agent teams
- recurring decision domains with repeated failure classes
- autonomous systems requiring evaluator maintenance

## Quick start

```bash
node --import tsx run.js --input ./examples/input.json
```

## Tool-call integration

This skill is wired to the consensus-interact contract boundary (via shared consensus-guard-core wrappers where applicable):
- readBoardPolicy
- getLatestPersonaSet / getPersonaSet
- writeArtifact / writeDecision
- idempotent decision lookup

This keeps board orchestration standardized across skills.
