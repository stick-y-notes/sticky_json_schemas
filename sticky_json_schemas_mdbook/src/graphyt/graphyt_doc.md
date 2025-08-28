# Graphyt Document

This document describes the JSON schema for a Graphyt document, which acts as a container for Graphyt notes, color palettes, and other content blocks.

## Schema

The schema for a Graphyt document is defined in `graphyt_doc.schema.json`.

```json
{{#include graphyt_doc.schema.json}}
```

## Document Structure

A Graphyt document is a JSON object with metadata and a flexible content structure.

### Document-Level Metadata

Each document contains:

- **id**: Unique identifier (UUID)
- **title**: User-defined document title
- **color**: Background color for the document (hex format)
- **tags**: Array of keywords or labels for categorization
- **createdAt**: ISO timestamp when document was created
- **updatedAt**: ISO timestamp when document was last modified
- **pinned**: Boolean indicating if document is pinned to top

### Content Types

The `content` field is an array of blocks. It can contain:

- **Graphyt Notes**: Full note objects, conforming to `graphyt_note.schema.json`.
- **Graphyt Palettes**: Color palette objects, conforming to `graphyt_palette.schema.json`.
- **Text Blocks**: Headings (`h1`-`h6`) and paragraphs (`p`).
- **Checkboxes**: Task items.

### h1

```json
{{#include ./doc_blocks/h1.schema.json}}
```

### h2

```json
{{#include ./doc_blocks/h2.schema.json}}
```

### h3

```json
{{#include ./doc_blocks/h3.schema.json}}
```

### h4

```json
{{#include ./doc_blocks/h4.schema.json}}
```

### h5

```json
{{#include ./doc_blocks/h5.schema.json}}
```

### h6

```json
{{#include ./doc_blocks/h6.schema.json}}
```

### p

```json
{{#include ./doc_blocks/p.schema.json}}
```

### blockquote

```json
{{#include ./doc_blocks/blockquote.schema.json}}
```

### code

```json
{{#include ./doc_blocks/code.schema.json}}
```

### hr

```json
{{#include ./doc_blocks/hr.schema.json}}
```

## Example

```json
{
  "id": "doc-123-abc",
  "title": "Project Phoenix Kick-off",
  "color": "#FFFFFF",
  "tags": ["project-phoenix", "kick-off", "planning"],
  "createdAt": "2025-08-28T10:00:00.000Z",
  "updatedAt": "2025-08-28T10:00:00.000Z",
  "pinned": true,
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
      "id": "550e8400-e29b-41d4-a716-446655440002",
      "title": "Action Items",
      "color": "#E8F5E8",
      "tags": ["actions", "team-a"],
      "createdAt": "2025-08-28T10:05:00.000Z",
      "updatedAt": "2025-08-28T10:05:00.000Z",
      "pinned": false,
      "content": [
        { "type": "checkbox", "label": "Define project scope", "checked": false },
        { "type": "checkbox", "label": "Assign team roles", "checked": false }
      ]
    },
    {
      "id": "c1b6a5f0-1b1f-4e3a-bf8a-2c2c5d7f1b1a",
      "name": "Project Color Palette",
      "colors": [
        "#FFC107",
        "#FF9800",
        "#FF5722"
      ]
    }
  ]
}
```
