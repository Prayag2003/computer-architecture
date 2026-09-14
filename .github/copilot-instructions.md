# Copilot instructions for this repository

## Project goal
Create easy to understand, college level notes for Computer Architecture and Organization. Zero to hero, visual, and exam ready.

## Core rules
- Use simple but accurate language
- Keep technical terms where needed
- Prefer mermaid diagrams, flowcharts, and tables over long paragraphs
- Use ASCII art only when mermaid cannot represent the concept (like bit-level register layouts)
- Do not repeat the same introduction in every video note
- Do not use em dashes
- Do not use LaTeX math notation. Write `2^12 = 4096` instead of `\(2^{12}\)`
- Keep the tone clear, readable, and exam friendly
- Include analogies and memory tricks where helpful
- Store lecture screenshots in the `public/` folder with naming format `Lec-XX-Description.png`
- Embed images in notes using `![description](../public/filename.png)`

## File structure
- [README.md](../README.md): Hub/index page with the roadmap
- [NOTES_GUIDE.md](../NOTES_GUIDE.md): Template and style rules for new notes
- [notes/](../notes/): All video-wise topic notes
- [public/](../public/): Lecture screenshots and reference images

## Structure for each new note
Follow the template in [NOTES_GUIDE.md](../NOTES_GUIDE.md):
1. Title with video number and topic
2. "Why this matters" section (1-2 lines)
3. Core concept explanation with diagrams
4. "How it works" with step by step breakdown
5. Key terms table
6. One example
7. Summary (3-5 bullet points)
8. Quick revision (3-5 one-liners)

## File naming
- Use `XX-topic-name.md` format in the notes folder
- Examples: `01-introduction-to-coa.md`, `04-instruction-cycle.md`

## Output quality checklist
- Clear and readable
- Conceptually correct
- At least one mermaid diagram per note
- No em dashes
- No LaTeX
- Simple language with accurate technical terms
- Summary and revision points present
- Useful for quick revision before exams

## Git commit conventions
- Do not use `git add .`. Stage files individually or by logical group
- Commit per topic or logical change, not everything in one go
- Commit message format:
  - New notes: `feat(topic-name): Add notes on [topic description]`
  - Config/docs updates: `docs: [what changed]`
- Examples:
  - `feat(common-bus): Add notes on common bus system using multiplexers`
  - `feat(basic-computer): Add notes on basic computer architecture with lecture diagrams`
  - `docs: Update roadmap, notes guide, and instructions with image support`
