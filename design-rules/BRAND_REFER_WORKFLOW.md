# Brand Design Refer Workflow

This document is the canonical workflow for creating future brand-specific Design Refer Skills inside the Design Rules ecosystem.

Use this protocol whenever the user provides a new brand guide, existing Skill, website reference, design library, campaign archive, Figma system, poster pack or visual identity source and asks to convert it into a reusable Agent Skill.

---

## Core pipeline

```text
Source Intake
→ Source Boundary
→ Brand DNA
→ Visual Families
→ Medium Adapters
→ Production Assets
→ Quality Gate
→ Same-Brief Benchmark
→ README Gallery
→ Router Registration
```

Do not skip directly from source material to a generic style prompt.

---

# Stage 0 — Source Intake

Inventory the supplied source material first.

Possible inputs:

- Brand Guide / PDF
- existing Agent Skill
- campaign poster archive
- website / landing page
- Figma design system
- image references
- source code / CSS tokens
- logo/background/icon/motion assets

Record what is actually supported by the source.

Do not silently add brand rules from memory.

---

# Stage 1 — Source Boundary

Create:

```text
SOURCE_NOTICES.md
references/source-notes.md
```

Separate:

```text
source-grounded rules
vs
inferred / derived adapters
```

A derived Web/PPT adapter must never be described as an official brand rule unless the source explicitly supports it.

---

# Stage 2 — Brand DNA

Create:

```text
references/brand-dna.md
```

Extract stable brand behavior across:

- color;
- typography;
- hierarchy;
- spacing;
- composition;
- imagery;
- logo treatment;
- motion;
- iconography;
- material / texture;
- information density;
- emotional temperature;
- anti-identity.

Write one compact Design Equation such as:

```text
A + B + C + D + E
```

The equation should explain the brand's behavior, not merely list colors.

---

# Stage 3 — Visual Families

Create:

```text
references/visual-families.md
```

Only create a Family when the source supports a **stable, repeatable visual behavior**.

Do not create arbitrary families just to reach a round number.

For every family document:

```text
ID
Chinese / human-readable name
Source evidence
Identity
Best for
Composition behavior
Color behavior
Typography behavior
Avoid list
```

A Family is not simply a different background color.

---

# Stage 4 — Medium Adapters

Create:

```text
references/medium-router.md
```

Separate:

```text
Source-grounded media
Derived adapters
```

Typical media:

```text
poster-social
web-ui
ppt-pdf
infographic
longform
motion
review-only
```

Derived adapters must preserve the Brand DNA while adapting to the usability requirements of the medium.

Never mechanically convert a poster layout into a website.

---

# Stage 5 — Production Assets

Recommended structure:

```text
assets/
├── brand/
├── backgrounds/
├── characters/
├── icons/
└── benchmark/
```

Rules:

- preserve approved logos and brand assets;
- do not redraw or recolor source assets unless the brand source explicitly allows it;
- never redistribute font binaries in Design Refer repositories;
- store font names, weights and usage rules only;
- if repository copies of large images are optimized, label them as optimized reference copies;
- preserve original source packages separately when needed.

---

# Stage 6 — Tokens

Create:

```text
tokens/<brand>.tokens.json
```

Prefer machine-readable values for:

- colors;
- gradients;
- typography names / weights;
- spacing / safe areas;
- family IDs;
- recurring dimensional rules.

Tokens should support Agent execution, not replace descriptive design logic.

---

# Stage 7 — Quality Gate

Create:

```text
references/quality-gate.md
```

Use a universal 0 / 1 / 2 score where practical.

Check at least:

1. communication clarity;
2. hierarchy;
3. family fidelity;
4. typography;
5. color discipline;
6. asset integrity;
7. medium fitness;
8. source fidelity;
9. originality;
10. brand anti-identity.

Define Hard Red Flags that force revision regardless of total score.

---

# Stage 8 — Same-Brief Benchmark

Every mature Brand Refer should be tested using one identical brief across every Family.

Purpose:

```text
same content
+ same medium
+ same constraints
+ different family only
```

This isolates Family behavior from content differences.

Create:

```text
assets/benchmark/<family>.jpg
assets/benchmark/visual-benchmark-grid.jpg
examples/<brand>-benchmark-prompts.md
```

The benchmark is not just marketing material. It is the visual unit test for the Skill.

---

# Stage 9 — README Gallery

A finished Brand Refer README should include:

```text
What this Skill is
Design Equation
Visual System at a glance
Visual Families
Family Gallery
Brand Tokens
Typography
Logo / Asset Discipline
Supported Mediums
Installation
Usage Examples
Benchmark Brief
Benchmark Prompt Cookbook
Quality Gate
Anti-Identity
Source Boundary
Router Integration
```

The repository homepage should visually demonstrate the design system without requiring the reader to open internal reference files first.

---

# Stage 10 — Router Registration

Register the new system in:

```text
design-rules/style-registry.json
```

Recommended maturity states:

```text
draft
→ source-ready
→ benchmark-backed
→ active
```

### `draft`
Source material exists but design DNA / families are incomplete.

### `source-ready`
Brand DNA, families, tokens, medium routes and quality gate are documented.

### `benchmark-backed`
The same-brief benchmark has been produced and reviewed.

### `active`
The system is trusted for automatic selection by `$design-rules-router`.

Do not allow `auto` routing to an unverified system merely because its repository exists.

---

# Canonical repository structure

```text
<brand>-design-refer/
├── README.md
├── SKILL.md
├── SOURCE_NOTICES.md
├── agents/
│   └── openai.yaml
├── assets/
│   ├── README.md
│   ├── brand/
│   ├── backgrounds/
│   └── benchmark/
├── examples/
│   ├── prompts.md
│   └── <brand>-benchmark-prompts.md
├── references/
│   ├── brand-dna.md
│   ├── visual-families.md
│   ├── medium-router.md
│   ├── quality-gate.md
│   └── source-notes.md
└── tokens/
    └── <brand>.tokens.json
```

Add brand-specific reference files only when the brand genuinely needs them, for example:

```text
references/character-system.md
references/motion.md
references/data-visualization.md
references/product-ui.md
```

---

# Naming convention

Repository:

```text
<brand>-design-refer
```

Skill:

```text
$<brand>-design-refer
```

Family IDs should be semantic and behavior-based rather than numbered style presets.

Good:

```text
blue-grid-reward
editorial-proof
industrial-dot-matrix
```

Avoid:

```text
style-01
style-A
cool-blue
```

unless the original source itself uses those names.

---

# Final principle

> **Build a reusable visual grammar, not a collection of screenshots.**

The goal of every Brand Design Refer is to let an Agent understand:

```text
what remains invariant
what can vary
which family to choose
how to adapt to the medium
what must never be invented
how to know when the design has failed
```

That is the standard path for all future Brand Refer Skills in this design library.
