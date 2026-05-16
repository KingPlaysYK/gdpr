# Validation Rules

For each completed row:

- `serial_number` exists
- `book_id` exists
- `category_id` is `29`
- Arabic source text is preserved
- `text_en` is non-empty when source `text` exists
- `literal_translation_en` is non-empty when source `text` exists
- word-by-word gloss exists or `word_by_word_path` points to it
- phrase notes exist when a phrase cannot be translated word-for-word cleanly

Before closing a chunk:

- No duplicate `serial_number` values in the completed checkpoint
- Output JSONL parses successfully
- Arabic text was not corrupted into mojibake

