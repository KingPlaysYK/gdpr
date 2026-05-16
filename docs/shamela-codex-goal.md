# Shamela Codex Translation Goal

## Goal

Translate the Shamela dataset using Codex as the active translation worker, starting with the Shamela language books category.

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

## Translation Layers

Each translated row should include:

- Original Arabic source text
- Readable English translation
- Literal English translation
- Word-by-word gloss
- Transliteration
- Phrase notes where word-by-word translation is misleading

## Storage Rule

GitHub stores plans, issues, schemas, progress notes, and code.

Large source files and translated dataset outputs should stay outside the GitHub repository, for example:

```text
D:\ShamelaTranslation
```

## Definition Of Done

This goal is complete when every accessible row in category `29 - كتب اللغة` has:

- `text_en`
- `literal_translation_en`
- word-by-word gloss data
- preserved Arabic source text
- preserved identifiers such as `serial_number`, `book_id`, `category_id`, `volume_number`, and `page_number`

