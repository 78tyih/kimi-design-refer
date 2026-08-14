# Design Rules Library

This repository now includes an upper-level **Design Rules Router** above `kimi-design-refer`.

Start here when you want the agent to **choose the visual system for you**, compare systems, review an existing design, or register a new aesthetic reference.

## Entry points

- [`design-rules/SKILL.md`](./design-rules/SKILL.md) — callable upper-level router
- [`design-rules/DESIGN_RULES.md`](./design-rules/DESIGN_RULES.md) — universal design rules
- [`design-rules/router.md`](./design-rules/router.md) — routing logic
- [`design-rules/style-registry.json`](./design-rules/style-registry.json) — registered systems
- [`design-rules/blend-policy.md`](./design-rules/blend-policy.md) — cross-system blend rules
- [`design-rules/quality-gate.md`](./design-rules/quality-gate.md) — 20-point universal review
- [`design-rules/prompt-interface.md`](./design-rules/prompt-interface.md) — reusable invocation format
- [`design-rules/taste-profile.md`](./design-rules/taste-profile.md) — default aesthetic biases

## Current architecture

```text
Design Rules Router
│
├── Universal rules
├── Taste profile
├── Style registry
├── Blend policy
└── Quality gate
        ↓
Registered Design Systems
        ↓
Kimi Design Refer  ← active / benchmark-backed
        ├── 7 Kimi Core Families
        └── 5 Zine Editorial Families
```

Planned registry slots currently include Linear, Stripe, Nothing and HTX design-reference systems. They are intentionally not routable until they are implemented and marked `active`.

## Quick invocation

```text
Use $design-rules-router.

Task: redesign this product homepage.
Medium: web-ui
Preferred system: auto

Choose the best registered design system and family,
apply at most one extension if necessary,
and run the universal quality gate before returning the result.
```
