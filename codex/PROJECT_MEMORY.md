# Project Memory

## Decisions

- GitHub is used for goals, issue tracking, schemas, and progress memory.
- The active umbrella goal issue is `#2`: complete all GitHub issues in this repository.
- Every Codex work item must be anchored to a GitHub issue. If work is not already covered by an issue, create or identify one first.
- Large dataset files and translated outputs stay outside GitHub.
- Local working folder is `D:\ShamelaTranslation`.
- First translation scope is Shamela category `29 - كتب اللغة - Language Books`.
- Translation must include readable English plus word-by-word gloss.
- Every main translated row must include structured `book_metadata` from `MoMonir/Shamela_Books_info`.
- The workflow uses Codex as the active translation worker.

## Dataset Facts

- Dataset: `mhaamh19/shamela_books_text_full`
- Total dataset rows: 7,552,019
- Total dataset books: 8,538
- First scope category: `29 - كتب اللغة`
- Category 29 books: 79
- Category 29 page rows extracted locally: 21,178
- Category 29 source shard found locally: `train-00042-of-00097.parquet`
- Category 29 metadata inventory: `D:\ShamelaTranslation\language_books\books_language_category_29.json`

## Translation Progress

- Completed language-books rows: 4
- Completed serial numbers: `6323683`, `6323684`, `6323685`, `6323686`
- Current next serial number: `6323687`
- Current book: `أبو تراب اللغوي وكتابه الاعتقاب`
- Current book_id: `22640`
- Current book author: `عبد الرزاق بن فراج الصاعدي`

## GitHub Facts

- Repo: `KingPlaysYK/gdpr`
- Umbrella goal issue: `#2` (`Goal: Complete all GitHub issues`) - https://github.com/KingPlaysYK/gdpr/issues/2
- Master translation issue: `#1` (`Goal: Translate all Shamela language books`)
- Setup commit: `efa456b`

## Open Questions

- Decide the default Codex chunk size for language-book pages.
- Decide whether chunk outputs should later be uploaded to Hugging Face Datasets.
- Decide how much word-by-word detail is required for very long pages.
