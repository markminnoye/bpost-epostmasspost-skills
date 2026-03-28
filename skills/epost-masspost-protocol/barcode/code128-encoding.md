> **When to use this file:** When implementing barcode generation in code (e.g., using a library or raw canvas) to ensure Code 128 Subset C is used correctly for Mail ID.

# Code 128 Encoding

All Mail ID barcodes must be encoded using the **Code 128 Subset C** symbology.

## Why Subset C?

- Subset C is designed specifically for **all-numeric** data.
- It encodes **two digits per character**, making the resulting barcode significantly shorter and easier to print on mail pieces.

## Symbology Parameters (Table 7)

| Parameter | Required Value |
|---|---|
| Symbology | Code 128 |
| Subset | Subset C (Numeric only) |
| Check Digit | Modulo 103 (standard for Code 128) |
| Start Character | 105 (Subset C Start) |
| Stop Character | 106 (Stop) |

## Encoding Process

1. **Start Character**: Start with the Start C character (decimal value 105).
2. **Data Encoding**: Group the 16-digit string into 8 pairs of digits.
   - Example: `0100456123456789` becomes `01`, `00`, `45`, `61`, `23`, `45`, `67`, `89`.
3. **Calculate Check Digit**: Use the standard Modulo 103 algorithm for Code 128.
4. **Stop Character**: End with the Stop character (decimal value 106).
5. **Quiet Zones**: Add the required quiet zones on both sides (minimum 5.0 mm).

## Check Digit Calculation Example

For the string `01004561`:

1. Start C (105) * 1 = 105
2. `01` (1) * 1 = 1
3. `00` (0) * 2 = 0
4. `45` (45) * 3 = 135
5. `61` (61) * 4 = 244
6. **Sum** = 105 + 1 + 0 + 135 + 244 = 485
7. **Modulo 103** = 485 % 103 = 73
8. **Check digit** = 73

## Implementation Tips

- Many libraries (e.g., `bwip-js` for Node.js, `python-barcode` for Python) support Code 128 Subset C automatically.
- Ensure the library is configured for **Start C** and **Modulo 103**.
- Validate the generated barcode with a barcode scanner app or hardware to confirm the numeric string is `16 digits`.

## Related Files

- For the numeric string structure, see [barcode-structure.md](./barcode-structure.md)
- For printing requirements, see [barcode-printing.md](./barcode-printing.md)
