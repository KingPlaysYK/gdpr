# Lexicon Workflow

## Purpose

The lexicon workflow extracts Arabic word entries from all Shamela language books and turns each discovered word into a sourced contextual English summary.

Tracker: #85

## Required Order

1. Finish the infrastructure definitions covered by #86 through #97.
2. Process each language book under its extraction issue, #98 through #176.
3. Build a global discovered-word manifest.
4. Generate one GitHub issue for every discovered normalized Arabic word.
5. Write each final word summary only under its word-specific issue.
6. Validate extraction coverage, issue coverage, and summary references before closing any tracker.

## Local Output Paths

Use local storage for data-heavy outputs:

```text
D:\ShamelaTranslation\lexicon\extracted
D:\ShamelaTranslation\lexicon\indexes
D:\ShamelaTranslation\lexicon\manifests
D:\ShamelaTranslation\lexicon\summaries
D:\ShamelaTranslation\lexicon\validation
```

## Extraction Rules

An extracted candidate may be a headword, explicitly discussed form, variant, singular/plural pair, definition, gloss, usage example, Quranic citation, Hadith citation, poetic citation, historical note, theological note, or cross-reference.

Every extracted candidate must include:

- source book metadata
- serial number and row location
- page and volume when present
- source text span
- candidate Arabic form
- normalized lookup key
- evidence type
- extraction issue number

Do not treat ordinary running prose as a word entry unless the book is explicitly defining, glossing, exemplifying, contrasting, or discussing the Arabic form.

## Contextual Translation Rules

- Translate entries contextually.
- Do not add literal translation layers.
- Do not add word-by-word gloss layers.
- Keep Arabic words, phrases, titles, and letters Arabic when they are being discussed as Arabic.
- Apply tashkeel to Arabic words or letters kept in English explanations when the form itself matters.

## Source-Priority Rules

Each final word summary must check sources in this order:

1. Quran
2. Hadith
3. Poetry
4. Other language-book evidence

Record whether each source class is present or absent. For Hadith, cite only what the corpus or authoritative source provides; do not invent grading or authentication claims.

## Final Summary Rules

A final word summary must:

- cite every substantive claim
- include all known references for supporting evidence
- compare definitions and usages across books
- distinguish attested information from inferred synthesis
- avoid unsupported theological or historical claims

No final summary may be written until the word has a dedicated GitHub issue.
