# Validation Rules

For each completed row:

- `serial_number` exists
- `book_id` exists
- `category_id` is `29`
- `book_metadata` exists on the main translated row
- `book_metadata.metadata_source` is `MoMonir/Shamela_Books_info`
- `book_metadata.author_name`, `book_metadata.book_link`, and `book_metadata.author_link` are preserved when present in the inventory
- Arabic source text is preserved
- `text_en` is non-empty when source `text` exists
- `literal_translation_en` is non-empty when source `text` exists
- word-by-word gloss exists or `word_by_word_path` points to it
- word-by-word rows include `serial_number`, `book_id`, `book_title`, and `author_name`
- phrase notes exist when a phrase cannot be translated word-for-word cleanly

Before closing a chunk:

- No duplicate `serial_number` values in the completed checkpoint
- Output JSONL parses successfully
- Arabic text was not corrupted into mojibake
