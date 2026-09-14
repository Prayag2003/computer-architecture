# Notes Guide: Template for Every Video Note

Use this structure when creating a new note. Each note should focus on one video/topic.

## File naming

- Use `XX-topic-name.md` format
- Examples: `01-introduction-to-coa.md`, `04-instruction-cycle.md`
- Keep names short and descriptive

## Template

```markdown
# Video X: [Topic Title]

## Why this matters
(1-2 lines connecting this topic to the big picture of COA. Why should you care?)

## Core Concept
(Main explanation. Use mermaid diagrams and tables here.)

## Reference Diagram
(Optional. If a lecture screenshot exists in `public/`, embed it with `![description](../public/filename.png)`)

## How it works
(Step by step breakdown. Use a mermaid flowchart to show the process.)

## Key Terms

| Term | Meaning | Example |
|------|---------|---------|
| ... | ... | ... |

## Example
(One concrete worked example with a diagram if possible)

## Summary
- Point 1
- Point 2
- Point 3

## Quick Revision
- One liner 1
- One liner 2
- One liner 3
```

## Style rules

1. **Simple language** without losing technical terms
2. **No em dashes** anywhere. Use commas, periods, or "and" instead
3. **No LaTeX math**. Write `2^12 = 4096` instead of `\(2^{12}\)`
4. **Mermaid diagrams** for all flowcharts, trees, and architecture visuals
5. **ASCII art** only when mermaid cannot represent it (like bit-level register layouts)
6. **Tables** for comparisons, register summaries, and term definitions
7. **Analogies and memory tricks** are encouraged
8. **One diagram minimum** per note
9. **No repeated intro content** across notes. The intro lives in `01-introduction-to-coa.md`
10. **Keep it exam friendly**. Summaries and revision points at the end of every note
11. **Lecture screenshots** go in the `public/` folder. Embed them with `![description](../public/filename.png)`. Use naming format `Lec-XX-Description.png`

## Quality checklist

Before finishing a note, verify:

- [ ] Title has video number and topic
- [ ] "Why this matters" section connects to the bigger picture
- [ ] At least one mermaid diagram is present
- [ ] Key terms table is filled if there are new terms
- [ ] Summary has 3-5 bullet points
- [ ] Quick revision has 3-5 one-liners
- [ ] No em dashes in the entire file
- [ ] No LaTeX notation
- [ ] Language is simple and clear
- [ ] Lecture screenshots (if any) are in `public/` and embedded correctly
