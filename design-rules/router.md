# Design Router

The Design Router chooses the design system **before** an agent starts styling.

## Routing input

Extract these fields from the user's brief:

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

### Suggested values

**medium**
- web-ui
- ppt-pdf
- poster-social
- infographic
- motion
- review-only

**communication_goal**
- explain
- persuade
- compare
- announce
- document
- explore
- demonstrate
- navigate

**information_density**
- whisper
- low
- medium
- high

**emotional_temperature**
- quiet
- neutral
- energetic
- dramatic

**evidence_level**
- abstract
- illustrative
- proof-heavy
- data-heavy

**interaction_level**
- none
- light
- functional
- dense

## Routing sequence

### Step 1 — Resolve medium

The actual medium has priority over style preference.

If the user asks for a website, choose a system that can preserve usability.
If the user asks for a research deck, prioritize exact typography and evidence structure.
If the user asks for a campaign poster, allow stronger abstraction and lower information density.

### Step 2 — Identify the dominant content behavior

Classify the content as one of:

- **system** — network, infrastructure, ecosystem, architecture;
- **evidence** — case study, rule, payout, result, proof;
- **knowledge** — research, map, taxonomy, index;
- **process** — workflow, transformation, simulation, sequence;
- **statement** — launch, slogan, manifesto, identity;
- **memory/editorial** — reflection, archive, note, culture;
- **comparison** — before/after, option A/B, platform comparison.

### Step 3 — Select a primary design system

Use `style-registry.json`.

Score systems against:

```text
medium_fit
content_fit
density_fit
emotion_fit
evidence_fit
brand_fit
```

Use a simple 0–3 score per dimension when comparison is useful.

Do not select a system solely because the user used a vague word like "高级" or "科技感".

### Step 4 — Select the family inside that system

For `kimi-design-refer`, route roughly as follows:

```text
system / infrastructure     → black-orbit
builder / experimental      → pixel-moon
measurement / analysis      → white-lab
knowledge / research map    → cosmic-index
evidence / comparison       → gray-proofboard
statement / identity        → kinetic-glyph
simulation / demo           → simulation-window
quiet archive               → zine/micro-archive
paired comparison           → zine/dual-memory
campaign focal tension      → zine/color-cutout
type-led identity           → zine/type-relic
research notes / mapping    → zine/orbit-notes
```

### Step 5 — Decide whether an extension is needed

Default: no blend.

Add an extension only when it solves a named design problem.

Examples:

- need more paper / editorial distance → add a Zine family;
- need stronger campaign tension → `zine/color-cutout`;
- need more archival quietness → `zine/micro-archive`;
- need typography to become the object → `zine/type-relic`.

### Step 6 — Apply the medium adapter

The same family behaves differently by medium.

Example:

```text
gray-proofboard poster
= one evidence fragment + large quiet field

gray-proofboard website
= evidence-led sections + real text + functional comparison modules

gray-proofboard deck
= title / evidence / comparison / conclusion rhythm
```

### Step 7 — Run the universal quality gate

Read `quality-gate.md` before returning the final artifact.

## Routing output

Before generation, the agent should be able to state internally or explicitly when helpful:

```text
Primary system: kimi-design-refer
Primary family: gray-proofboard
Extension: zine/micro-archive
Extension intensity: light
Medium: poster-social
Density: whisper
Reason: proof-heavy research content requiring editorial restraint
```

## Auto-select behavior

If the user does not specify a family:

1. choose one family;
2. do not ask the user to pick unless several options are genuinely equivalent and the distinction matters;
3. briefly explain the choice when the task is exploratory;
4. proceed with the design.

## Anti-routing patterns

Do not:

- choose `black-orbit` for every technology brief;
- choose Zine merely because the user asks for minimalism;
- choose `simulation-window` just because the content contains charts;
- average multiple families because each has one attractive trait;
- ignore the real medium to preserve a poster-like aesthetic.
