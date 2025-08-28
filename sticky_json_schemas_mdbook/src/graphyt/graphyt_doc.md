# Graphyt Document

This document describes the JSON schema for a Graphyt document, which acts as a container for Graphyt notes and color palettes.

## Schema

The schema for a Graphyt document is defined in `graphyt_doc.schema.json`.

```json
{{#include graphyt_doc.schema.json}}
```

## Document Structure

A Graphyt document is a JSON object that can contain two main properties:

- **notes**: An array of Graphyt notes. Each item in the array must conform to the `graphyt_note.schema.json`.
- **palettes**: An array of Graphyt color palettes. Each item in the array must conform to the `graphyt_palette.schema.json`.

## Example

```json
{
  "notes": [
    {
      "id": "550e8400-e29b-41d4-a716-446655440002",
      "title": "Design Sprint Planning",
      "color": "#E8F5E8",
      "tags": ["sprint", "planning", "team-a", "ux"],
      "createdAt": "2025-01-14T08:00:00.000Z",
      "updatedAt": "2025-01-15T11:30:00.000Z",
      "pinned": false,
      "content": [
        { "type": "h2", "text": "Sprint Goals" },
        { "type": "p", "text": "Focus on user onboarding flow and core feature wireframes." }
      ]
    }
  ],
  "palettes": [
    {
      "id": "c1b6a5f0-1b1f-4e3a-bf8a-2c2c5d7f1b1a",
      "name": "Sunset Vibes",
      "colors": [
        "#FFC107",
        "#FF9800",
        "#FF5722",
        "#F44336"
      ]
    }
  ]
}
```
