# Translation Queue

## Queue Strategy

The full category 29 queue is local because it is data-heavy:

```text
D:\ShamelaTranslation\language_books\pages_category_29_language_books.jsonl
```

GitHub tracks queue strategy and progress, not the full queue data.

## Current Queue

```text
scope: category_id 29
category: كتب اللغة
rows: 21,178
books: 79
status: ready locally
```

## Completed

```text
6323683
6323684
6323685
6323686
6323687
```

## Next

```text
6323688
```

## Queue Rules

- Work in small chunks.
- Never translate a row twice unless doing a repair pass.
- Use `serial_number` as the stable row ID.
- Update the checkpoint after each completed chunk.
- Keep local chunk outputs outside GitHub.
