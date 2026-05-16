# Language Books Lexicon Plan

## Category

```text
category_id: 29
category: كتب اللغة
English: Language Books
```

## Inventory

The companion Shamela metadata dataset reports 79 books in this category.

The text dataset extraction found 21,178 page rows for category `29`.

## Metadata Source

Every extracted word-entry record and every final word summary must be able to cite metadata copied from the local category inventory:

```text
D:\ShamelaTranslation\language_books\books_language_category_29.json
```

The metadata source is `MoMonir/Shamela_Books_info`. Preserve author name, author link, book link, publisher, edition, pages, volumes, pagination, category, and source inventory identifiers when present.

## Work Units

- Book translation issues: #6 through #84
- Lexicon tracker: #85
- Lexicon infrastructure issues: #86 through #97
- Lexicon extraction issues: #98 through #176

The final synthesis unit is one issue per discovered normalized Arabic word. Those word-specific issues are generated after extraction creates the global discovered-word manifest.

## Workflow

1. Complete or identify the GitHub issue that covers the atomic task.
2. Repair mojibake before reading Arabic text.
3. Process one book under its lexicon extraction issue.
4. Extract Arabic headwords, definitions, variants, singular/plural mentions, examples, Quranic citations, Hadith citations, poetic citations, historical notes, theological notes, and cross-references.
5. Preserve exact source references: book title, author, publisher, edition, page, volume, serial number, row location, and source span when available.
6. Add extracted candidates to the per-book JSONL output and global discovered-word manifest.
7. Generate one issue for every discovered normalized Arabic word.
8. Under each word issue, look up that word across all language books and produce a sourced contextual English summary.
9. Validate that all claims are sourced and that the source-priority policy was checked.

## Source-Priority Rule

For every final word summary, check evidence in this order:

1. Quranic usage
2. Hadith usage
3. Poetic usage
4. Other language-book definitions and examples

If a source class is absent, record that absence explicitly. Do not invent citations or authentication claims.
