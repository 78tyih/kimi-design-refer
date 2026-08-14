# Blend Policy

Blending is optional. The default design decision is **one primary system with no extension**.

Use blending only when the secondary system solves a specific problem that the primary system does not solve well enough on its own.

## Allowed structure

Preferred:

```text
1 primary system
+ 0–1 extension system
+ 1 medium adapter
```

Avoid:

```text
3+ equal systems
```

because this usually produces visual averaging rather than a coherent design language.

## Dominance rule

When two systems are combined, define dominance explicitly.

Suggested ratios:

- light extension: 75/25
- medium extension: 60/40
- extension-led: 35/65, only when the extension is intentionally the visible surface language

The primary system should still control at least one of:

- composition logic;
- hierarchy;
- information behavior;
- interaction behavior;
- evidence grammar.

## Trait-level blending

Blend traits, not entire visual identities.

Good:

```text
gray-proofboard structure
+ micro-archive paper surface
```

```text
cosmic-index knowledge hierarchy
+ orbit-notes annotation distance
```

```text
white-lab measurement logic
+ restrained zine print texture on a report cover
```

Weak:

```text
black-orbit + pixel-moon + white-lab + color-cutout + glassmorphism
```

## Problem-driven extension selection

Use an extension only to solve a named need.

| Need | Useful extension |
| --- | --- |
| more archival distance | `zine/micro-archive` |
| explicit A/B relationship | `zine/dual-memory` |
| stronger campaign focal tension | `zine/color-cutout` |
| typography should become the subject | `zine/type-relic` |
| sparse research-note atmosphere | `zine/orbit-notes` |

## Medium limits

### Web UI

Prefer light extensions. Surface texture and editorial styling must not reduce readability, responsiveness or interaction clarity.

### PPT / PDF

Medium extensions are acceptable on title pages, chapter pages and selected evidence pages. Dense data pages should reduce stylistic noise.

### Poster / Social

The widest blend range is acceptable because the artifact can privilege one visual proposition.

### Infographic

Keep blending low. Accuracy, labels and semantic grouping dominate.

### Motion

Blend motion grammar separately from surface styling. One system should own timing / movement behavior.

## Color conflict rule

If two systems define different color logic, select one system as color authority.

Example:

```text
Primary: gray-proofboard
Extension: zine/color-cutout
Color authority: zine/color-cutout
```

Then gray-proofboard keeps structure while the zine system owns the single cobalt anchor.

## Typography conflict rule

Assign roles rather than mixing type systems randomly.

Example:

```text
Display: editorial serif from zine extension
Body: neutral sans from medium adapter
Metadata: mono from Kimi core
```

## Texture conflict rule

Texture should behave as one reproduction environment.

Do not combine unrelated effects such as:

- glossy 3D;
- heavy Xerox;
- glassmorphism;
- pixel dithering;
- film grain;

all at once.

## Stop condition

If the combined prompt needs more than one paragraph to explain how the styles should coexist, the blend is probably too complex.

Simplify to one primary system and one narrow extension trait.
