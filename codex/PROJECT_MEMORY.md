# Project Memory

## Decisions

- GitHub is used for goals, issue tracking, schemas, and progress memory.
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

- Completed language-books rows: 1
- Completed serial numbers: `6323683`
- Current next serial number: `6323684`
- Current book: `أبو تراب اللغوي وكتابه الاعتقاب`
- Current book_id: `22640`
- Current book author: `عبد الرزاق بن فراج الصاعدي`

## GitHub Facts

- Repo: `KingPlaysYK/gdpr`
- Master goal issue: `#1`
- Setup commit: `efa456b`

## Open Questions

- Decide the default Codex chunk size for language-book pages.
- Decide whether chunk outputs should later be uploaded to Hugging Face Datasets.
- Decide how much word-by-word detail is required for very long pages.
