# Graphyt Website

This document describes the JSON schema for a Graphyt website, designed for drag and drop website building.

## Schema

The schema for a Graphyt website is defined in `graphyt_website.schema.json`.

```json
{{#include graphyt_website.schema.json}}
```

## Website Structure

A Graphyt website is a JSON object with metadata and a flexible content structure, similar to the document schema but with additional web-specific blocks.

### Website-Level Metadata

Each website can optionally contain:

- **id**: Unique identifier (string)
- **title**: User-defined website title
- **color**: Primary color for the website (hex format)
- **tags**: Array of keywords or labels for categorization
- **createdAt**: ISO timestamp when website was created
- **updatedAt**: ISO timestamp when website was last modified

---

### Content Types

The `content` field is an array of blocks. In addition to the standard document blocks, it can contain web-specific blocks:

- [button.schema.json](./graphyt_blocks/button.schema.json)
- [image.schema.json](./graphyt_blocks/image.schema.json)
- [nft_display.schema.json](./graphyt_blocks/nft_display.schema.json)
- [ft_display.schema.json](./graphyt_blocks/ft_display.schema.json)

### button

```json
{{#include ./graphyt_blocks/button.schema.json}}
```

### image

```json
{{#include ./graphyt_blocks/image.schema.json}}
```

### nft_display

```json
{{#include ./graphyt_blocks/nft_display.schema.json}}
```

### ft_display

```json
{{#include ./graphyt_blocks/ft_display.schema.json}}
```

---

## Example

```json
{
  "id": "my-website",
  "title": "My Awesome Website",
  "content": [
    {
      "type": "h1",
      "text": "Welcome to My Website"
    },
    {
      "type": "p",
      "text": "This is a paragraph about my website."
    },
    {
      "type": "button",
      "label": "Click Me!",
      "link": "https://example.com",
      "emoji": "👉"
    },
    {
      "type": "image",
      "url": "https://example.com/image.jpg",
      "alt": "An example image"
    },
    {
      "type": "nft_display"
    },
    {
      "type": "ft_display"
    }
  ]
}
```