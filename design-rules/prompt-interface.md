# Prompt Interface

Use this compact interface when asking an agent to route and execute a design task.

## Minimal form

```text
Use the Design Rules Library.

Task: [what needs to be designed]
Medium: [web-ui / ppt-pdf / poster-social / infographic / motion / review-only]
Content: [brief or source material]

Choose the most appropriate registered design system and family.
Explain the choice briefly, then execute.
```

## Controlled form

```text
Use the Design Rules Library.

Task: ...
Medium: ...
Communication goal: ...
Audience: ...
Information density: whisper / low / medium / high
Emotional temperature: quiet / neutral / energetic / dramatic
Evidence level: abstract / illustrative / proof-heavy / data-heavy
Interaction level: none / light / functional / dense

Preferred system: auto / kimi-design-refer / ...
Preferred family: auto / ...
Extension: none / auto / ...
Blend intensity: light / medium / extension-led

Must preserve:
- ...

Avoid:
- ...

Output:
- final artifact
- routing decision
- family / system used
- quality-gate result when useful
```

## Router-first command

For ambiguous visual briefs:

```text
Use the Design Rules Library as the upper-level art director.

Do not style immediately.
First classify the medium, content behavior, density, emotional temperature and evidence level.
Then select one primary registered design system and one family.
Use at most one extension only if it solves a specific problem.
Apply the medium adapter and universal quality gate.
```

## Review command

```text
Use the Design Rules Library in review mode.

Target medium: web-ui
Target system: auto
Target family: auto

Inspect this design and identify:
1. the design system it currently resembles;
2. hierarchy / focal / negative-space issues;
3. whether the style is structural or merely decorative;
4. the three highest-impact fixes.

Score it using design-rules/quality-gate.md.
```

## Benchmark command

```text
Use the Design Rules Library.

Create a benchmark using the same content across multiple registered families.
Keep the content, medium and aspect ratio constant.
Change only the family-level visual grammar.
Return one output per family and a comparison note.
```

## New-system registration command

```text
Use the Design Rules Library.

Analyze these brand references and create a new Design Refer system.
Do not copy sample identity or exact compositions.
Separate:
- fixed DNA;
- variable families;
- medium adapters;
- color / type rules;
- avoid list;
- quality gate.

Then register the system in design-rules/style-registry.json using systems/_template.md.
```
