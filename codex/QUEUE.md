# Lexicon Queue

## Queue Strategy

The full category 29 queue is local because it is data-heavy:

```text
D:\ShamelaTranslation\language_books\pages_category_29_language_books.jsonl
```

GitHub tracks queue strategy, issue coverage, and progress. Large extracted outputs stay local.

## Current Corpus

```text
scope: category_id 29
category: كتب اللغة
rows: 21,178
books: 79
status: ready locally
```

## GitHub Queue Coverage

- Lexicon tracker: #85
- Infrastructure tasks: #86 through #97
- Per-book extraction tasks: #98 through #176
- Fresh-start cleanup: #177 through #183
- Word summary tasks: generated after the discovered-word manifest exists

## Fresh-Start State

Pre-policy generated translated-row outputs, word-by-word outputs, stale translation checkpoints, and stale run notes were deleted before lexicon extraction began. The queue is fresh for the sourced lexicon workflow.

## Next

```text
#89 - Lexicon: Implement extraction and indexing script
```

## Queue Rules

- Work in GitHub issue order unless a dependency requires otherwise.
- Never start an uncovered atomic task.
- Use `book_id` and `serial_number` as stable source identifiers.
- Use a normalized Arabic key only for cross-book lookup, not as a replacement for the cited Arabic form.
- Update local manifests/checkpoints after each completed issue.
