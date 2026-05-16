# Word-By-Word Translation Schema

The project records both readable translation and word-by-word translation.

## Main Row Fields

```json
{
  "serial_number": "string",
  "category_id": "string",
  "category": "Arabic category",
  "category_en": "English category",
  "book_title": "Arabic title",
  "book_title_en": "English title",
  "book_id": "string",
  "page_number": "string or null",
  "volume_number": "string or null",
  "text": "Arabic source text",
  "foot_note": "Arabic source footnote or null",
  "text_en": "Readable English translation",
  "literal_translation_en": "Literal English rendering",
  "foot_note_en": "English footnote translation or null",
  "word_by_word_path": "Path to word-by-word JSONL",
  "translation_worker": "codex",
  "source_dataset": "mhaamh19/shamela_books_text_full"
}
```

## Word-By-Word Row Fields

```json
{
  "serial_number": "string",
  "token_index": 1,
  "arabic": "Arabic token",
  "transliteration": "Latin transliteration",
  "literal_gloss": "word-level English gloss",
  "contextual_gloss": "context-aware English gloss",
  "notes": "optional grammar or phrase note"
}
```

## Rule

Arabic often does not map cleanly one word to one English word. Use phrase notes when a literal gloss would mislead the reader.

