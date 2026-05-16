# Source Reference Schema

Every extracted record and final summary claim must be traceable to source data.

## Required Fields

```json
{
  "id": "stable local reference id",
  "source_kind": "language_book | quran | hadith | poetry | metadata | other",
  "book_id": "string or null",
  "book_title_ar": "string or null",
  "author_name_ar": "string or null",
  "publisher_ar": "string or null",
  "edition": "string or null",
  "page_number": "string or null",
  "volume_number": "string or null",
  "serial_number": "string or null",
  "row_index": "integer or null",
  "source_span_ar": "Arabic source text span",
  "source_span_en": "contextual English translation or null",
  "book_link": "string or null",
  "author_link": "string or null",
  "metadata_source": "string or null",
  "extraction_issue": "GitHub issue URL",
  "word_issue": "GitHub issue URL or null"
}
```

## Reference Rules

- Preserve available author, publisher, edition, page, and volume metadata.
- If a field does not exist in the source, leave it null. Do not infer it silently.
- For language-book evidence, include `serial_number` and `source_span_ar`.
- For Quran evidence, include surah and ayah identifiers when available.
- For Hadith evidence, include collection, book/chapter, number, or the exact source wording when available.
- For poetry, include poet, meter, verse, or cited source when available.
- A summary sentence that cannot point to at least one source reference must be rewritten or removed.
