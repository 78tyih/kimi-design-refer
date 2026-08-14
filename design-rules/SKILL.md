---
name: design-rules-router
description: "Upper-level AI art director and design router. Classify a design brief, choose a registered design system and family, control blending, adapt to the target medium, and run a universal quality gate before output."
---

# Design Rules Router

Use this Skill when the user wants design work but has not already committed to one visual family, or when the task needs art direction, system selection, style comparison, review, or registration of a new visual system.

## 1. Read the universal layer

Read:

- `DESIGN_RULES.md`
- `taste-profile.md`

Universal rules control hierarchy, focal logic, evidence integrity, medium fitness, readability, originality and reduction.

Style-specific systems may add rules but should not silently violate the universal layer.

## 2. Route the brief

Read `router.md`.

Extract:

```text
medium
communication_goal
content_type
information_density
emotional_temperature
interaction_level
evidence_level
brand_constraints
audience
output_format
```

If the user did not specify a family, choose one rather than asking them to browse every option.

## 3. Select a registered design system

Read `style-registry.json`.

Choose one primary system using medium fit, content fit, density fit, emotion fit, evidence fit and brand fit.

Current mature system:

- `kimi-design-refer`

Planned systems may appear in the registry, but do not route to them until their status is `active` and their system card exists.

## 4. Select a family

Read the selected system card under `systems/` and then the system's own Skill / references.

For Kimi Design Refer, use `systems/kimi-design-refer.md` and `../SKILL.md`.

## 5. Blend only if necessary

Read `blend-policy.md`.

Default:

```text
1 primary system
+ no extension
```

If blending solves a named problem, use at most one extension and define dominance explicitly.

Do not average multiple visual identities.

## 6. Adapt to the real medium

Do not preserve style at the expense of medium truth.

- web-ui → usability and responsive hierarchy first;
- ppt-pdf → exact copy and reading order first;
- poster-social → one proposition and one focal event;
- infographic → semantic accuracy first;
- motion → temporal hierarchy first;
- review-only → diagnose before redesigning.

## 7. Execute

Use the selected system's detailed rules and tools to produce the artifact.

When useful, expose a compact routing note:

```text
System: ...
Family: ...
Extension: ...
Medium: ...
Reason: ...
```

Do not turn routing explanation into a long preamble when the user simply wants the output.

## 8. Quality gate

Read `quality-gate.md` plus the selected system's own quality gate.

A final artifact should pass both:

```text
Universal quality
AND
Family fidelity
```

Revise high-impact failures before returning.

## 9. Register new systems

When the user asks to add a new brand / aesthetic reference:

1. analyze references;
2. separate fixed DNA, variable grammar and sample residue;
3. create a system card from `systems/_template.md`;
4. define families only when they change stable grammar;
5. benchmark the families on one shared brief;
6. register the system in `style-registry.json`;
7. mark it `benchmark-backed` only after examples exist.

## Prompt interface

For reusable invocation formats, read `prompt-interface.md`.
