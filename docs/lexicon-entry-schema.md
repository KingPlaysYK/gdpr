# Lexicon Entry Schema

## Extracted Word-Entry Record

Per-book extraction outputs should be JSONL. Each line represents one source-backed candidate.

```json
{
  "record_type": "extracted_word_entry",
  "extraction_issue": "https://github.com/KingPlaysYK/gdpr/issues/98",
  "book_id": "string",
  "serial_number": "string",
  "row_location": {
    "page_number": "string or null",
    "volume_number": "string or null",
    "source_span_start": "integer or null",
    "source_span_end": "integer or null"
  },
  "source_reference": {
    "book_title_ar": "string",
    "author_name_ar": "string or null",
    "publisher_ar": "string or null",
    "edition": "string or null",
    "book_link": "string or null",
    "author_link": "string or null",
    "metadata_source": "MoMonir/Shamela_Books_info"
  },
  "headword_ar": "Arabic word or phrase as printed",
  "headword_with_tashkeel": "Arabic word with tashkeel when supplied or recoverable from context",
  "normalized_key_ar": "Arabic lookup key without unstable orthographic noise",
  "entry_type": "definition | variant | singular_plural | example | quran | hadith | poetry | historical | theological | cross_reference | other",
  "source_span_ar": "Arabic source text span",
  "contextual_translation_en": "contextual English translation when the span itself is translated",
  "related_forms_ar": [
    {
      "form_ar": "Arabic form",
      "relation": "singular | plural | variant | root | derived_form | unknown"
    }
  ],
  "notes": "brief extraction note or null",
  "extracted_by": "codex",
  "extracted_at": "YYYY-MM-DD"
}
```

## Final Word Summary Record

Final summaries should be written only after a word-specific GitHub issue exists.

```json
{
  "record_type": "sourced_word_summary",
  "word_issue": "https://github.com/KingPlaysYK/gdpr/issues/...",
  "headword_ar": "Arabic headword with tashkeel when discussed",
  "normalized_key_ar": "Arabic lookup key",
  "contextual_translation_en": "contextual English translation",
  "linguistic_breakdown": {
    "root_ar": "Arabic root or null",
    "pattern_ar": "Arabic pattern or null",
    "part_of_speech": "string or null",
    "morphology_notes": "sourced notes"
  },
  "meaning_in_usage": "sourced contextual explanation",
  "singular_forms_ar": ["Arabic form"],
  "plural_forms_ar": ["Arabic form"],
  "examples": [
    {
      "example_ar": "Arabic source example",
      "example_en": "contextual English translation",
      "source_reference_id": "string"
    }
  ],
  "source_priority": {
    "quran": {
      "status": "found | not_found | not_checked",
      "references": ["source_reference_id"]
    },
    "hadith": {
      "status": "found | not_found | not_checked",
      "references": ["source_reference_id"]
    },
    "poetry": {
      "status": "found | not_found | not_checked",
      "references": ["source_reference_id"]
    },
    "language_books": {
      "status": "found | not_found | not_checked",
      "references": ["source_reference_id"]
    }
  },
  "historical_information": "sourced notes or null",
  "theological_usage": "sourced notes or null",
  "cross_book_summary": "sourced synthesis across all available language-book evidence",
  "source_references": [
    {
      "id": "string",
      "book_id": "string",
      "book_title_ar": "string",
      "author_name_ar": "string or null",
      "publisher_ar": "string or null",
      "page_number": "string or null",
      "volume_number": "string or null",
      "serial_number": "string",
      "source_span_ar": "Arabic source text span"
    }
  ],
  "validation": {
    "all_claims_sourced": true,
    "cross_book_index_checked": true,
    "word_issue_exists": true
  }
}
```

## Rules

- Use `null` or an empty array for absent evidence.
- Do not invent author, publisher, page, volume, Quran, Hadith, poetry, historical, or theological data.
- Do not mark a source class as `not_found` unless it was actually checked.
