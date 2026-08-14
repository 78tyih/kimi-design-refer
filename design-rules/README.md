# Design Rules Library

`design-rules/` is the meta layer above individual visual families.

Its job is not to define another visual style. It decides **how an agent should choose, combine, adapt and review design systems** before rendering a website, deck, poster, infographic or motion piece.

## Layer model

```text
User brief
   ↓
Universal Design Rules
   ↓
Design Router
   ↓
Style Registry
   ↓
Primary Design System
   ↓
Family / Extension
   ↓
Medium Adapter
   ↓
Quality Gate
   ↓
Final Output
```

## Files

- `DESIGN_RULES.md` — universal rules that apply regardless of style.
- `router.md` — decision logic for choosing a design system and family.
- `style-registry.json` — machine-readable registry of available systems.
- `blend-policy.md` — rules for mixing systems without visual mush.
- `quality-gate.md` — cross-system art-direction review criteria.
- `prompt-interface.md` — standard invocation contract for agents.
- `taste-profile.md` — the current taste biases of this library.
- `systems/kimi-design-refer.md` — registry card for the current Kimi system.
- `systems/_template.md` — template for future systems such as Linear, Stripe, Nothing or HTX.

## Principle

> Choose a system before choosing decoration.

The router should always resolve the design problem first: medium, communication goal, information density, emotional temperature, evidence type and interaction needs. Only then should it select a style system.

## Current status

The registry currently contains one mature system:

- `kimi-design-refer` — 7 Kimi Core families + 5 Zine Editorial Extension families.

Future systems can be added without rewriting the universal rules.
