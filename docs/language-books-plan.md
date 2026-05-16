# Language Books Translation Plan

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

Each translated row must include a `book_metadata` object copied from the local category inventory:

```text
D:\ShamelaTranslation\language_books\books_language_category_29.json
```

The metadata source is `MoMonir/Shamela_Books_info`. Preserve author name, author link, book link, publisher, edition, pages, volumes, pagination, category, and source inventory identifiers.

## First Books In Queue

| Book ID | Arabic Title | Author |
|---:|---|---|
| 133417 | النوادر في اللغة | أبو زيد الأنصاري |
| 7508 | إصلاح المنطق | ابن السكيت أبو يوسف يعقوب بن إسحاق |
| 5420 | القلب والإبدال | ابن السكيت أبو يوسف يعقوب بن إسحاق |
| 29605 | الملاحن | أبو بكر محمد بن الحسن بن دريد الأزدي |
| 17819 | المذكر والمؤنث | محمد بن القاسم بن محمد بن بشار أبو بكر الأنباري |
| 6925 | الألفاظ | أبو منصور الباحث محمد بن سهل بن المرزبان الكرخي |
| 14565 | المقصور والممدود | ابن ولاد أبو العباس أحمد بن محمد بن الوليد التميمي المصري |
| 14569 | المقصور والممدود | أبو عمر محمد بن عبد الواحد البغدادي الزاهد |
| 14443 | تصحيح الفصيح وشرحه | أبو محمد عبد الله بن جعفر بن محمد بن درستويه |
| 37469 | الإتباع | عبد الواحد بن علي الحلبي أبو الطيب اللغوي |

## Workflow

1. Pull the next untranslated language-book row.
2. Merge the matching `book_metadata` record by `book_id`.
3. Repair mojibake if the Arabic text is corrupted.
4. Translate with Codex.
5. Add readable English translation.
6. Add literal translation.
7. Add word-by-word gloss.
8. Save output locally.
9. Record progress in GitHub Issues.
