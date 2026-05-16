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
  "book_metadata": {
    "metadata_source": "MoMonir/Shamela_Books_info",
    "metadata_local_inventory": "D:\\ShamelaTranslation\\language_books\\books_language_category_29.json",
    "sn": 7020,
    "book_id": "string",
    "book_title": "Arabic title",
    "book_title_en": "English title",
    "book_link": "https://shamela.ws/book/...",
    "author_name": "Arabic author name or null",
    "author_name_en": "English transliteration or null",
    "author_year": "death year or null",
    "nickname": "nickname or null",
    "author_link": "https://shamela.ws/author/...",
    "author_id": "string or null",
    "editor": "editor or null",
    "publisher": "Arabic publisher or null",
    "publisher_en": "English publisher translation or null",
    "edition": "edition or null",
    "pages": "page count or null",
    "volumes": "volume count or null",
    "pagination": "Arabic pagination note or null",
    "pagination_en": "English pagination note or null",
    "category": "Arabic category",
    "category_en": "English category",
    "category_id": "string"
  },
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
  "book_id": "string",
  "book_title": "Arabic title",
  "author_name": "Arabic author name or null",
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
