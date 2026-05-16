# Project Memory

## Decisions

- GitHub is used for goals, issue tracking, schemas, and progress memory.
- The active umbrella goal issue is `#2`: complete all GitHub issues in this repository.
- Every Codex work item must be anchored to a GitHub issue. If work is not already covered by an issue, create or identify one first.
- Large dataset files, extracted lexicon outputs, indexes, manifests, and final summaries stay outside GitHub.
- Local working folder is `D:\ShamelaTranslation`.
- Active scope is Shamela category `29 - كتب اللغة - Language Books`.
- Active project goal is a sourced lexicon, not row-only translation.
- Active translation policy is contextual-only: no literal translation layer and no word-by-word gloss layer.
- Arabic words, phrases, title terms, and letters being discussed as Arabic must stay Arabic with tashkeel when the form itself is being discussed.
- Every final word summary must check Quran usage first, Hadith usage next, poetry after that, then other language-book evidence.
- Every final word summary must be sourced.
- No final word summary may begin until a word-specific GitHub issue exists.

## Dataset Facts

- Dataset: `mhaamh19/shamela_books_text_full`
- Total dataset rows: 7,552,019
- Total dataset books: 8,538
- First scope category: `29 - كتب اللغة`
- Category 29 books: 79
- Category 29 page rows extracted locally: 21,178
- Category 29 source shard found locally: `train-00042-of-00097.parquet`
- Category 29 metadata inventory: `D:\ShamelaTranslation\language_books\books_language_category_29.json`

## GitHub Facts

- Repo: `KingPlaysYK/gdpr`
- Umbrella goal issue: `#2` (`Goal: Complete all GitHub issues`)
- Master language-books issue: `#1`
- Contextual-only policy issue: `#3`
- Pre-policy repair issue: `#4`, superseded by fresh-start deletion
- Contextual continuation issue: `#5`
- Dataset translation issues: `#6` through `#84`
- Sourced lexicon tracker: `#85`
- Lexicon infrastructure issues: `#86` through `#97`
- Lexicon extraction issues: `#98` through `#176`
- Fresh-start cleanup tracker: `#177`
- Fresh-start cleanup issues: `#178` through `#183`
- Setup commit: `efa456b`

## Fresh-Start Cleanup

The following serials had generated pre-policy translation outputs, but those outputs were deleted and no longer count as retained work:

```text
6323683
6323684
6323685
6323686
6323687
6323688
6323689
6323690
6323691
```

Deleted local generated artifacts included translated-row JSONL, word-by-word JSONL, stale translation checkpoints, and the old `logs\codex_runs\next_chunk.md` run note. Source corpus files and metadata inventory files were kept.

## Next Work

Continue with issue #89:

```text
Lexicon: Implement extraction and indexing script
```

## Open Questions

- Decide whether final lexicon summaries should later be uploaded to Hugging Face Datasets.
- Decide which external Quran/Hadith/poetry corpora or local sources should be accepted when the language books cite them incompletely.
