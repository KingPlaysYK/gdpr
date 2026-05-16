# Shamela Translation Project

This repository tracks a Codex-assisted translation project for the Shamela dataset.

Primary dataset:

https://huggingface.co/datasets/mhaamh19/shamela_books_text_full

## Current Goal

Start with Shamela category:

```text
29 - كتب اللغة - Language Books
```

Current extracted scope:

- 79 language books
- 21,178 page rows
- Word-by-word gloss required
- Readable English translation required
- Arabic source text preserved
- Structured book metadata required, including author, Shamela links, publisher, edition, pagination, and source metadata dataset

## Docs

- [Shamela Codex Goal](docs/shamela-codex-goal.md)
- [Language Books Plan](docs/language-books-plan.md)
- [Word-By-Word Schema](docs/word-by-word-schema.md)
- [Codex Long-Run Workflow](docs/codex-long-run-workflow.md)

## Codex Operating System

This repo is set up so Codex can resume work across many sessions without needing the whole previous chat context.

Start every new Codex session here:

1. Read [codex/CONTEXT_PACK.md](codex/CONTEXT_PACK.md)
2. Read [codex/NEXT_ACTION.md](codex/NEXT_ACTION.md)
3. Complete one small chunk
4. Update [codex/SESSION_LOG.md](codex/SESSION_LOG.md)
5. Update [codex/NEXT_ACTION.md](codex/NEXT_ACTION.md)

## Storage

GitHub is for goals, issues, schemas, notes, and progress.

Large source files and translated outputs should be stored locally or in dataset storage, not committed to this repo.
