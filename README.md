# humanify

A Claude Code skill that diagnoses, drafts and revises prose so that it reads as accountable writing for a real reader, genre and purpose. It works on English (normalized to en-US) and Spanish (normalized to es-CO).

Natural prose is treated here as successful writing within a genre, not as informality, imperfection or resemblance to a detector's "human" class. The skill never optimizes for an AI detector, never adds typos, slang, anecdotes or invented detail to seem human, and never claims a text is human-written.

## How it works

For an existing text:

`inspect -> map -> diagnose -> reconcile -> report -> human gate -> revise -> integrate -> verify -> deliver`

For a new document:

`establish contract -> map claims and warrants -> propose structure -> human gate -> draft -> self-diagnose -> revise -> verify -> deliver`

- **Fidelity first.** Names, numbers, dates, definitions, quotations, citations, modality, conditions, causal force and uncertainty are registered as protected content before any change.
- **Human gate.** The full diagnosis, an anchored issue ledger and one revision plan come before any edit. The user approves the plan, amends it or excludes issue IDs.
- **Internal consistency.** Claims, terms, numbers, cross-references and annexes are checked against each other, without importing outside facts.
- **Long documents.** Semantic units, a resumable review record and coverage accounting, with as many workers as the document needs and one coordinator that owns the revised copy.
- **Files.** Pasted text, `.txt`, `.md` and `.docx`; PDF as a diagnostic source; spreadsheets as evidence. Word, PDF and spreadsheet mechanics are delegated to the `docx`, `pdf` and `xlsx` skills. The source is never overwritten.

## Contents

| File | Holds |
|---|---|
| `skills/humanify/SKILL.md` | the contract, routing, phases and delivery |
| `references/editorial-principles.md` | the editorial decision framework, with its research sources |
| `references/diagnostic-rubric.md` | the diagnostic dimensions, issue ledger schema and completion test |
| `references/english-us.md` | en-US realization |
| `references/spanish-colombia.md` | es-CO realization (in Spanish) |
| `references/file-handling.md` | rules per input and output format |
| `references/long-document-workflow.md` | orchestration for long or interconnected documents |
| `references/evaluation.md` | final verification gates |

## Install

As a plugin, inside Claude Code:

```
/plugin marketplace add baqata/humanify
/plugin install humanify@humanify
```

Or as a personal skill:

```bash
git clone https://github.com/baqata/humanify.git
cp -R humanify/skills/humanify ~/.claude/skills/
```

## Use

The skill runs only when called explicitly: `/humanify` followed by pasted text or a file path (`/humanify:humanify` when installed as a plugin). For `.docx`, `.pdf` and spreadsheet inputs, the `docx`, `pdf` and `xlsx` skills must be available.

## License

MIT
