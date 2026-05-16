# Context Pack

## Project

Build a sourced Arabic-to-English lexicon from Shamela language books using Codex.

## GitHub Repo

https://github.com/KingPlaysYK/gdpr

## Goal Issues

- Umbrella goal: https://github.com/KingPlaysYK/gdpr/issues/2
- Sourced lexicon tracker: https://github.com/KingPlaysYK/gdpr/issues/85
- Contextual-only policy: https://github.com/KingPlaysYK/gdpr/issues/3
- Pre-policy repair: https://github.com/KingPlaysYK/gdpr/issues/4
- Contextual continuation tracker: https://github.com/KingPlaysYK/gdpr/issues/5

Every Codex work item must be anchored to a GitHub issue before work starts.

## Dataset

https://huggingface.co/datasets/mhaamh19/shamela_books_text_full

## Current Scope

```text
category_id: 29
category: كتب اللغة
English: Language Books
```

Known extracted local scope:

- 79 books
- 21,178 page rows
- Source shard: `train-00042-of-00097.parquet`

## Issue Maps

- Book translation issues: #6 through #84
- Lexicon infrastructure issues: #86 through #97
- Book extraction issues: #98 through #176

The final synthesis unit is one generated GitHub issue per discovered normalized Arabic word.

## Local Working Folder

```text
D:\ShamelaTranslation
```

Important local paths:

```text
D:\ShamelaTranslation\language_books\books_language_category_29.json
D:\ShamelaTranslation\language_books\pages_category_29_language_books.jsonl
D:\ShamelaTranslation\lexicon\extracted
D:\ShamelaTranslation\lexicon\indexes
D:\ShamelaTranslation\lexicon\manifests
D:\ShamelaTranslation\lexicon\summaries
D:\ShamelaTranslation\lexicon\validation
D:\ShamelaTranslation\checkpoints
```

Legacy pre-policy outputs may exist under `D:\ShamelaTranslation\translated`; they require repair under issue #4 before being treated as compliant.

## Active Policy

- Translate entries contextually.
- Do not add literal translation layers.
- Do not add word-by-word gloss layers.
- Keep Arabic words, phrases, title terms, and letters Arabic when they are being discussed as Arabic.
- Apply tashkeel to Arabic forms kept inside English explanations when the form itself is being discussed.
- Do not write final lexical claims without source references.

## Required Docs

- `docs/lexicon-workflow.md`
- `docs/lexicon-entry-schema.md`
- `docs/source-reference-schema.md`
- `codex/NEXT_ACTION.md`
- `codex/PROJECT_MEMORY.md`
- `codex/SESSION_LOG.md`

## Rules

- Do not try to load the whole dataset into context.
- Work one GitHub issue at a time.
- If a future task does not already have a specific issue, create or identify one before doing the work.
- Do not write a final word summary until a word-specific issue exists.
