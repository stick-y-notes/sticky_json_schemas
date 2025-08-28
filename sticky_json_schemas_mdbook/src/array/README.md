# Array Schemas
JSON schemas for different types of arrays.

- [array.schema.json](./array.schema.json)
- [array_of_numbers.schema.json](./array_of_numbers.schema.json)
- [array_of_strings.schema.json](./array_of_strings.schema.json)


## Generic Array

A schema for a basic array with unrestricted item types.

```json
{{#include array.schema.json}}
```

## Array of Strings

This schema validates that an array contains only string items.

```json
{{#include array_of_strings.schema.json}}
```

## Array of Numbers

This schema validates that an array contains only number items.

```json
{{#include array_of_numbers.schema.json}}
```



---

copyright: 2025 by sleet.near