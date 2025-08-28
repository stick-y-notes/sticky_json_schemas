# Bible Book Schema

This schema is for a book of the Bible.

- [bible_book.schema.json](./bible_book.schema.json)

This is used by the [SUNBIBLE](https://github.com/SunBible-dev) project.

## Book

A schema for a book of the Bible.

```json
{{#include bible_book.schema.json}}
```

### Sample

```json
{
    "book": "1 Chronicles",
    "chapters": [
        {
            "chapter": "1",
            "verses": [
                {
                    "verse": "1",
                    "text": "Adam, Sheth, Enosh,"
                },
                {
                    "verse": "2",
                    "text": "Kenan, Mahalaleel, Jered,"
                },
                {
                    "verse": "3",
                    "text": "Henoch, Methuselah, Lamech,"
                },
                {
                    "verse": "4",
                    "text": "Noah, Shem, Ham, and Japheth."
                },
                {
                    "verse": "5",
                    "text": "The sons of Japheth; Gomer, and Magog, and Madai, and Javan, and Tubal, and Meshech, and Tiras."
                }
            ]
        }
    ]
}
```

---

copyright: 2025 by sleet.near
