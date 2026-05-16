# Shamela Codex Goal

## Goal

Build a sourced English lexicon from the Shamela language-books corpus, using Codex as the active extraction, translation, and synthesis worker.

Dataset:

https://huggingface.co/datasets/mhaamh19/shamela_books_text_full

## Current Scope

Start with category:

```text
29 - كتب اللغة - Language Books
```

Local extraction found:

- Language category books: 79
- Language category page rows: 21,178
- Source parquet shard: `train-00042-of-00097.parquet`

## GitHub Issue Map

- Umbrella goal: #2
- Original language-books goal: #1
- Contextual-only policy: #3
- Repair pre-policy row outputs: #4, superseded by fresh-start deletion
- Contextual continuation tracker: #5
- Book translation issue map: #6 through #84
- Sourced lexicon tracker: #85
- Lexicon infrastructure: #86 through #97
- Per-book lexicon extraction: #98 through #176

No atomic task may begin without a GitHub issue. A final word summary may not begin until that discovered word has its own issue.

## Active Translation Policy

The active policy is contextual-only:

- Translate the entry in context, nothing more or less.
- Do not add literal translation layers.
- Do not add word-by-word gloss layers.
- Preserve the Arabic source text.
- When an Arabic word, phrase, title term, or letter is being discussed as Arabic, keep it Arabic.
- Apply tashkeel to Arabic words or letters kept inside English explanations when the form itself is being discussed.

## Lexicon Requirements

Each discovered Arabic word entry must ultimately receive a sourced English summary containing:

- Arabic headword and normalized key
- Contextual English translation
- Linguistic breakdown and morphology
- Meaning in usage and contextual explanation
- Singular and plural forms when present in the books
- Example sentences/usages
- Historical information when present
- Theological usage when present
- Quranic evidence first, Hadith evidence next, poetic evidence after that, and other language-book evidence after those
- Full references for every supporting source

## Storage Rule

GitHub stores plans, issues, schemas, progress notes, and code.

Large source files, extracted word-entry records, cross-book indexes, and final lexicon outputs should stay outside the GitHub repository, for example:

```text
D:\ShamelaTranslation
```

## Definition Of Done

This goal is complete when:

- All 79 language books have been inspected for Arabic word entries.
- Stale pre-policy generated translation outputs have been deleted and are not treated as retained work.
- Every extracted word-entry candidate has source references.
- A global discovered-word manifest exists.
- Every discovered normalized Arabic word has its own GitHub issue.
- Every word issue contains a contextual, sourced English summary.
- Validation confirms no language-book row, extracted entry, or discovered word is left uncovered.
