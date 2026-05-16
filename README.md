# Shamela Language-Books Lexicon Project

This repository tracks a Codex-assisted project for the Shamela language-books corpus.

Primary dataset:

https://huggingface.co/datasets/mhaamh19/shamela_books_text_full

## Current Goal

Build a sourced Arabic lexicon from Shamela category `29 - كتب اللغة - Language Books`.

Current extracted scope:

- 79 language books
- 21,178 page rows
- Dataset translation issue map: #6 through #84
- Lexicon tracker: #85
- Lexicon infrastructure issues: #86 through #97
- Lexicon extraction issue map: #98 through #176

## Active Translation Policy

- Translate entries contextually, nothing more or less.
- Do not create literal translation layers.
- Do not create word-by-word gloss layers.
- If an Arabic word, phrase, title term, or letter is being referred to as Arabic, keep it Arabic.
- Apply tashkeel to Arabic words or letters kept inside English explanations when the form itself is being discussed.
- Do not write final lexical claims without source references.

## Lexicon Deliverable

For every Arabic word entry discovered in the language-books corpus, produce a sourced summary that includes:

- Arabic headword and normalized lookup key
- Contextual English translation
- Linguistic and morphological breakdown
- Meaning in usage and contextual explanation
- Singular and plural forms when present in the books
- Example sentences or usages
- Historical information when present
- Theological usage when present
- Source-priority evidence: Quran first, Hadith next, poems after that, then other language-book evidence
- Full references: book title, author, publisher, page, volume, serial number, and metadata links when available

Every discovered normalized word must have its own GitHub issue before final synthesis begins.

## Docs

- [Shamela Codex Goal](docs/shamela-codex-goal.md)
- [Language Books Plan](docs/language-books-plan.md)
- [Lexicon Workflow](docs/lexicon-workflow.md)
- [Lexicon Entry Schema](docs/lexicon-entry-schema.md)
- [Source Reference Schema](docs/source-reference-schema.md)
- [Legacy Word-By-Word Schema](docs/word-by-word-schema.md)
- [Codex Long-Run Workflow](docs/codex-long-run-workflow.md)

## Codex Operating System

This repo is set up so Codex can resume work across many sessions without needing the whole previous chat context.

Start every new Codex session here:

1. Read [codex/CONTEXT_PACK.md](codex/CONTEXT_PACK.md)
2. Read [codex/NEXT_ACTION.md](codex/NEXT_ACTION.md)
3. Complete only work covered by a GitHub issue
4. Update [codex/SESSION_LOG.md](codex/SESSION_LOG.md)
5. Update [codex/NEXT_ACTION.md](codex/NEXT_ACTION.md)

## Storage

GitHub is for goals, issues, schemas, notes, and progress.

Large source files, extracted lexicon records, and final dataset outputs should be stored locally or in dataset storage, not committed to this repo.
