# Universal Quality Gate

Run this after the family-specific quality gate and before returning the final artifact.

Score each dimension from 0–2:

- `0` = fails or missing
- `1` = acceptable but weak
- `2` = deliberate and strong

Recommended pass threshold: **16 / 20**.

## 1. Communication clarity

Can a viewer understand the primary proposition without reading every annotation?

## 2. Hierarchy

Is there a clear primary, secondary and evidence layer?

## 3. Focal discipline

Is there one dominant visual event or functional region?

## 4. Negative-space discipline

Does empty space help reading order and emphasis rather than simply remaining unused?

## 5. Evidence integrity

Are real facts, numbers, rules and comparisons represented accurately and legibly?

## 6. Medium fitness

Does the artifact behave correctly for its medium?

For UI: usable.
For deck/PDF: readable.
For poster: immediate.
For infographic: accurate.
For motion: temporally legible.

## 7. Color discipline

Does each color have a job? Are accents still meaningful?

## 8. Typography discipline

Are display, body, metadata and data typography clearly assigned?

## 9. System fidelity

Can the chosen design system / family be recognized from structure and behavior, not merely from surface decoration?

## 10. Originality and reduction

Does the work avoid copied sample residue, generic AI visual clichés and unnecessary detail?

## Red flags

Any of the following should trigger revision even if the numeric score passes:

- important text rendered inaccurately;
- inaccessible interaction or unreadable type;
- fake data presented as real;
- multiple equal focal points without intentional comparison;
- visual family reduced to decorative motifs only;
- unauthorized logo / campaign copying;
- generic blue-purple AI styling replacing the selected family;
- extension system overwhelming core usability.

## Review output

When reviewing an existing design, return:

```text
Overall score: X / 20
Primary system fidelity: X / 2

Highest-impact fixes:
1. ...
2. ...
3. ...

Keep:
- ...
```

Prioritize changes with the highest visual and communication impact. Do not produce a long list of minor polish notes before addressing hierarchy, focal logic and evidence clarity.
