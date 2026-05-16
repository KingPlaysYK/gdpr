# Next Action

## Current Task

Continue the sourced lexicon project under GitHub issue #85.

The next unfinished infrastructure task is:

```text
#89 - Lexicon: Implement extraction and indexing script
```

Do not resume row-by-row translation as the next task. The active project is now extracting Arabic word entries, building a cross-book lexicon, generating word-specific issues, and writing sourced contextual summaries.

## Input

Use local queue:

```text
D:\ShamelaTranslation\language_books\pages_category_29_language_books.jsonl
```

Use metadata inventory:

```text
D:\ShamelaTranslation\language_books\books_language_category_29.json
```

## Output

Use local lexicon folders:

```text
D:\ShamelaTranslation\lexicon\extracted
D:\ShamelaTranslation\lexicon\indexes
D:\ShamelaTranslation\lexicon\manifests
D:\ShamelaTranslation\lexicon\summaries
D:\ShamelaTranslation\lexicon\validation
```

## Completion Checklist

- [ ] Confirm the work is covered by GitHub issue #89.
- [ ] Create local lexicon output folders if missing.
- [ ] Implement deterministic extraction/indexing script.
- [ ] Ensure extraction records include source references.
- [ ] Ensure output follows `docs/lexicon-entry-schema.md` and `docs/source-reference-schema.md`.
- [ ] Update `codex/SESSION_LOG.md`.
- [ ] Update this file with the next issue.

## Blocking Rule

No final word summary may be written until the discovered word has its own GitHub issue.
