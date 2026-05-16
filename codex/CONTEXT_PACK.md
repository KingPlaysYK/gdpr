# Context Pack

## Project

Translate Shamela language books into English using Codex.

## GitHub Repo

https://github.com/KingPlaysYK/gdpr

## Master Issue

https://github.com/KingPlaysYK/gdpr/issues/1

## Dataset

https://huggingface.co/datasets/mhaamh19/shamela_books_text_full

## Current Scope

Start with:

```text
category_id: 29
category: كتب اللغة
English: Language Books
```

Known extracted local scope:

- 79 books
- 21,178 page rows
- Source shard: `train-00042-of-00097.parquet`

## Local Working Folder

```text
D:\ShamelaTranslation
```

Important local paths:

```text
D:\ShamelaTranslation\language_books\books_language_category_29.json
D:\ShamelaTranslation\language_books\pages_category_29_language_books.jsonl
D:\ShamelaTranslation\translated\codex_chunks
D:\ShamelaTranslation\translated\word_by_word
D:\ShamelaTranslation\checkpoints
```

## Required Translation Layers

Each translated row needs:

- readable English translation
- literal English translation
- word-by-word gloss
- transliteration
- phrase notes when literal gloss is misleading
- preserved Arabic source text

## Output Schema

Use:

```text
docs/word-by-word-schema.md
```

## Rule

Do not try to load the whole dataset into context. Work one small chunk at a time and record progress in this repo.

