# System Card — [system-id]

Use this template when adding a new Design Refer system.

## Identity

- **ID:** `[system-id]`
- **Status:** draft / active / deprecated
- **Maturity:** exploratory / reference-backed / benchmark-backed
- **Role:** [one-line design-system role]
- **Skill entry:** [path or repository]

## Source boundaries

Document:

- public references used;
- license / attribution requirements;
- what is observed;
- what is inferred;
- what must not be copied.

## Core philosophy

Write one compact design equation:

```text
[trait]
+ [trait]
+ [trait]
+ [trait]
```

## Best-fit content

Strong fit:

- ...

Weak fit:

- ...

## Medium support

Score 0–3:

| Medium | Fit |
| --- | --- |
| web-ui | 0–3 |
| ppt-pdf | 0–3 |
| poster-social | 0–3 |
| infographic | 0–3 |
| motion | 0–3 |
| review-only | 0–3 |

## Families

Only create a family when it changes stable visual grammar, not merely coordinates or color.

| Family | Primary behavior | Best for |
| --- | --- | --- |
| `...` | ... | ... |

## Fixed DNA

Traits that should survive across most outputs:

- ...

## Variable system

Traits that may change without breaking identity:

- ...

## Color logic

Define:

- base palette;
- accent logic;
- status colors;
- prohibited defaults.

## Typography logic

Define type by job:

- display;
- body;
- metadata;
- numeric/data;
- special family type.

## Composition grammar

Define:

- focal behavior;
- negative-space range;
- grid / alignment behavior;
- density behavior;
- recurring structures.

## Signature visual primitives

Examples:

- ...

## Motion grammar

If relevant:

- entry behavior;
- transition behavior;
- motion verbs;
- timing character;
- avoid list.

## Medium adapters

Explain how the system changes for:

- web-ui;
- ppt-pdf;
- poster-social;
- infographic;
- motion.

## Avoid

- ...

## Quality gate

List 5–10 system-specific checks.

## Benchmark

Create a benchmark using the same brief across every family before marking the system `benchmark-backed`.

Store examples under:

```text
assets/benchmark/[system-id]/
```

## Registry update

After the system card is stable:

1. add it to `../style-registry.json`;
2. define medium fit;
3. define content fit;
4. add family routing tags;
5. update the upper README / registry docs.
