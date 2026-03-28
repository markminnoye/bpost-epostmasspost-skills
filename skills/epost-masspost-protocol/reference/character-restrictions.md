> **When to use this file:** When sanitizing input data for XML/TXT files to prevent encoding errors or invalid character rejections by bpost.

# Character Restrictions

All data exchanged with the MAIL ID system must adhere to strict character encoding rules to ensure compatibility with sorting machines and database systems.

## Supported Character Set

- **Codepage**: ISO-8859-1 (Latin-1)
- All characters within this set are generally allowed, **except** for those explicitly restricted below.

## Prohibited Characters (Table 11)

| Character | Description | Restriction |
|---|---|---|
| `<` | Less than | Prohibited in XML content (use `&lt;`) |
| `>` | Greater than | Prohibited in XML content (use `&gt;`) |
| `&` | Ampersand | Prohibited in XML content (use `&amp;`) |
| `'` | Single quote | Prohibited in XML content (use `&apos;`) |
| `"` | Double quote | Prohibited in XML content (use `&quot;`) |
| `|` | Pipe | **Strictly Prohibited** in TXT files (delimiter) |
| `\` | Backslash | Reserved for escaping in TXT files |

## Field-Specific Constraints

### Numeric Fields
- Only digits `0-9` are allowed.
- No spaces, dashes, or punctuation.

### Alphanumeric Fields
- Letters `A-Z`, `a-z`, digits `0-9`, and generic punctuation.
- Avoid using special symbols (e.g., emojis, non-Latin characters) as they are likely to be rejected.

## Handling Restricted Characters

1. **XML Encoding**: Always use standard XML entity escapes for the five special XML characters (`<`, `>`, `&`, `'`, `"`).
2. **Sanitization**: Remove or replace any unsupported characters before generating the file.
3. **Pipe character**: In TXT format, any literal `|` must be escaped with a backslash (`\|`).

## Related Files

- For encoding and compression, see [../transport/compression-and-encoding.md](../transport/compression-and-encoding.md)
- For address-specific rules, see [addressing-rules.md](./addressing-rules.md)
