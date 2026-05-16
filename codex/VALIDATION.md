# Validation Rules

## Extracted Word Entries

For each extracted record:

- `record_type` is `extracted_word_entry`
- `extraction_issue` points to the relevant GitHub issue
- `book_id` exists
- `serial_number` exists
- `source_reference` exists
- Arabic source span is preserved
- `headword_ar` exists
- `normalized_key_ar` exists
- `entry_type` is one of the schema values
- page and volume are preserved when present
- author, publisher, book link, and author link are preserved when present in metadata
- Arabic text was not left as mojibake after repair

## Final Word Summaries

For each final summary:

- `record_type` is `sourced_word_summary`
- `word_issue` points to the word-specific GitHub issue
- `headword_ar` exists and uses tashkeel when the Arabic form is being discussed
- `contextual_translation_en` is non-empty
- every substantive claim has at least one source reference
- cross-book index was checked
- Quran evidence status is recorded
- Hadith evidence status is recorded
- poetry evidence status is recorded
- language-book evidence status is recorded
- singular/plural forms are sourced when present
- examples are sourced and translated contextually
- synonyms or near-synonyms are sourced when present
- differences between synonyms or near-synonyms are sourced
- examples identify whether they support the definition, synonym distinction, morphology, usage, or source-priority evidence

## Forbidden In Active Outputs

- new `literal_translation_en` requirements
- new `word_by_word_path` requirements
- unsourced historical claims
- unsourced theological claims
- unsourced synonym claims
- unsourced claims that two words differ in meaning, usage, register, dialect, form, or context
- invented author, publisher, page, volume, Quran, Hadith, or poetry references

## Before Closing A Book Extraction Issue

- Every row in the book serial range was inspected
- Output JSONL parses successfully
- Candidate count is recorded
- Per-book unique candidate list exists
- Global discovered-word manifest was updated

## Before Closing A Word Summary Issue

- All source-priority checks were completed
- Summary references resolve to extracted records or accepted source records
- Validation report is saved locally
- GitHub issue includes the final summary or points to its local output path
