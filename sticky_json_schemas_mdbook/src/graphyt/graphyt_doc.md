# Graphyt Document

This document describes the JSON schema for a Graphyt document

## Schema

The schema for a Graphyt document is defined in `graphyt_doc.schema.json`.

```json
{{#include graphyt_doc.schema.json}}
```

## Document Structure

A Graphyt document is a JSON object with metadata and a flexible content structure.

### Document-Level Metadata

Each document can optionally contain:

- **id**: Unique identifier (string)
- **title**: User-defined document title
- **color**: Background color for the document (hex format)
- **tags**: Array of keywords or labels for categorization
- **createdAt**: ISO timestamp when document was created
- **updatedAt**: ISO timestamp when document was last modified
- **pinned**: Boolean indicating if document is pinned to top

---

### Content Types

The `content` field is an array of blocks. It can contain:

- [blockquote.schema.json](./graphyt_blocks/blockquote.schema.json)
- [checkbox.schema.json](./graphyt_blocks/checkbox.schema.json)
- [code.schema.json](./graphyt_blocks/code.schema.json)
- [h1.schema.json](./graphyt_blocks/h1.schema.json)
- [h2.schema.json](./graphyt_blocks/h2.schema.json)
- [h3.schema.json](./graphyt_blocks/h3.schema.json)
- [h4.schema.json](./graphyt_blocks/h4.schema.json)
- [h5.schema.json](./graphyt_blocks/h5.schema.json)
- [h6.schema.json](./graphyt_blocks/h6.schema.json)
- [hr.schema.json](./graphyt_blocks/hr.schema.json)
- [p.schema.json](./graphyt_blocks/p.schema.json)


### h1

```json
{{#include ./graphyt_blocks/h1.schema.json}}
```

### h2

```json
{{#include ./graphyt_blocks/h2.schema.json}}
```

### h3

```json
{{#include ./graphyt_blocks/h3.schema.json}}
```

### h4

```json
{{#include ./graphyt_blocks/h4.schema.json}}
```

### h5

```json
{{#include ./graphyt_blocks/h5.schema.json}}
```

### h6

```json
{{#include ./graphyt_blocks/h6.schema.json}}
```

### p

```json
{{#include ./graphyt_blocks/p.schema.json}}
```

### blockquote

```json
{{#include ./graphyt_blocks/blockquote.schema.json}}
```

### code

```json
{{#include ./graphyt_blocks/code.schema.json}}
```

### hr

```json
{{#include ./graphyt_blocks/hr.schema.json}}
```

---

## Website Builder

For drag and drop website building, see the [Graphyt Website Schema](./graphyt_website.md).

---

## Example

```json
{
  "id": "my-document",
  "title": "Project Phoenix Kick-off",
  "content": [
    {
      "type": "h1",
      "text": "Project Phoenix Kick-off Meeting"
    },
    {
      "type": "p",
      "text": "This document contains all the notes and resources for the kick-off meeting."
    },
    {
      "type": "h2",
      "text": "Agenda"
    },
    {
      "type": "p",
      "text": "The following topics will be discussed:"
    },
    {
        "type": "blockquote",
        "text": "The minutes of this meeting will be distributed to all attendees."
    },
    {
        "type": "hr"
    },
    {
        "type": "code",
        "text": "console.log('Hello, World!');"
    },
    {
        "type": "checkbox",
        "label": "Define project scope",
        "checked": false
    }
  ]
}
```
