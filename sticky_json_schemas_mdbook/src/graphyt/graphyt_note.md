# GRAPHYT NOTE FORMAT

This document describes the JSON schema for a single note in the Graphyt application.

## Schema

The schema for a Graphyt note is defined in
[graphyt_note.schema.json](./graphyt_note.schema.json).

## Note Structure

Each note in Graphyt is a standalone JSON object with rich content capabilities and comprehensive metadata tracking.

### Note-Level Metadata

Each note contains:

- **id**: Unique identifier (UUID)
- **title**: User-defined note title
- **color**: Background color for the note card (hex format)
- **tags**: Array of keywords or labels for categorization
- **createdAt**: ISO timestamp when note was created
- **updatedAt**: ISO timestamp when note was last modified
- **pinned**: Boolean indicating if note is pinned to top

### Content Types

The `content` field is an array of blocks, each with a specific `type`.

| Type        | Description                                                                 |
|-------------|-----------------------------------------------------------------------------|
| `h1`–`h6`    | Headings for structure and hierarchy. Contains a `text` field.              |
| `p`         | Paragraph text for descriptions or notes. Contains a `text` field.          |
| `checkbox`  | Task item with a `label` and a `checked` state.                             |
| `date`      | ISO-formatted date string (e.g. `"2025-09-10"`). Stored in a `value` field. |

## Example

```json
{
  "id": "550e8400-e29b-41d4-a716-446655440002",
  "title": "Design Sprint Planning",
  "color": "#E8F5E8",
  "tags": ["sprint", "planning", "team-a", "ux"],
  "createdAt": "2025-01-14T08:00:00.000Z",
  "updatedAt": "2025-01-15T11:30:00.000Z",
  "pinned": false,
  "content": [
    {
      "type": "date",
      "value": "2025-01-20"
    },
    { "type": "h2", "text": "Sprint Goals" },
    { "type": "p", "text": "Focus on user onboarding flow and core feature wireframes." },
    { "type": "h3", "text": "Deliverables" },
    { "type": "checkbox", "label": "User journey mapping", "checked": true },
    { "type": "checkbox", "label": "Low-fi wireframes", "checked": false },
    { "type": "checkbox", "label": "Stakeholder review session", "checked": false }
  ]
}
```
