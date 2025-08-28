# Graphyt Color Palette

This document describes the JSON schema for a color palette in the Graphyt ecosystem. This can be used as an extension to the core Graphyt note format.

## Schema

The schema for a Graphyt color palette is defined in `graphyt_palette.schema.json`.

[View Schema](graphyt_palette.schema.json)

## Palette Structure

Each palette is a JSON object with the following properties:

- **id**: Unique identifier (UUID) for the palette.
- **name**: A user-defined name for the palette.
- **colors**: An array of hex color strings (e.g., `"#RRGGBB"`).

## Example

```json
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
```
