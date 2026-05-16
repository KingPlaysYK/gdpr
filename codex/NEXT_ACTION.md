# Next Action

## Current Task

Create the next translation chunk for Shamela language books category `29 - كتب اللغة`.

The next untranslated row is:

```text
serial_number: 6323687
book_id: 22640
book_title: أبو تراب اللغوي وكتابه الاعتقاب
page_number: 348
volume_number: 114
```

## Input

Use local queue:

```text
D:\ShamelaTranslation\language_books\pages_category_29_language_books.jsonl
```

## Output

Save translated chunk locally under:

```text
D:\ShamelaTranslation\translated\codex_chunks
```

Save word-by-word gloss locally under:

```text
D:\ShamelaTranslation\translated\word_by_word
```

Merge book metadata from:

```text
D:\ShamelaTranslation\language_books\books_language_category_29.json
```

## Completion Checklist

- [ ] Pick row `6323687`
- [ ] Add `book_metadata` from `MoMonir/Shamela_Books_info`
- [ ] Preserve Arabic source text
- [ ] Add readable English translation
- [ ] Add literal English translation
- [ ] Add word-by-word gloss
- [ ] Add phrase notes if needed
- [ ] Update local checkpoint
- [ ] Add GitHub progress note or session log entry

## Previous Chunk

Completed row:

```text
serial_number: 6323686
book_id: 22640
book_title: أبو تراب اللغوي وكتابه الاعتقاب
```

Local outputs:

```text
D:\ShamelaTranslation\translated\codex_chunks\language_books\language_books_6323686.jsonl
D:\ShamelaTranslation\translated\word_by_word\language_books\serial_6323686.jsonl
```
