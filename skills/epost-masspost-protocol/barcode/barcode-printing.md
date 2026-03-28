> **When to use this file:** When designing the mail piece layout, choosing font size, or positioning the barcode on the envelope.

# Barcode Printing

## Barcode Placement (Table 4)

| Placement | Specification |
|---|---|
| **Envelope size** | Standard (up to C5 size) / Large (up to C4 size) |
| **Horizontal Position** | Center, left-justified, or right-justified |
| **Vertical Position** | Above or below the address block (must follow a blank line) |
| **Minimum Margins** | 5.0 mm on all sides (left, right, top, bottom) |

## Dimensions and Quality (Table 5)

| Parameter | Required Value |
|---|---|
| Narrow bar width | Minimum 0.25 mm / Maximum 0.50 mm (recommended: 0.33 mm) |
| Barcode height | Minimum 10.0 mm / Maximum 15.0 mm |
| Barcode length | Based on Code 128 encoding (calculated from encoded text) |
| Barcode color | **Black only** (RGB: 0,0,0) |
| Background color | **White only** (RGB: 255,255,255) |
| Print resolution | Minimum 300 DPI (non-interpolated) |

## Barcode Quiet Zone (Table 6)

| Region | Minimum Quiet Zone |
|---|---|
| Left of barcode | 5.0 mm |
| Right of barcode | 5.0 mm |
| Top/Bottom of barcode | 2.0 mm |

## Barcode Orientation

- All barcodes must be printed **horizontally** (parallel to the address).
- Barcode rotation is not allowed.

## Barcode Content (Self-Verification)

- The barcode must contain the **full Mail ID string** (e.g., `0100456123456789`).
- The barcode string is composed of `FCC` + `CustomerID` + `MailPieceNumber`.
- For more details on the string structure, see [barcode-structure.md](./barcode-structure.md).

## Related Files

- For encoding steps, see [code128-encoding.md](./code128-encoding.md)
- For data structure, see [barcode-structure.md](./barcode-structure.md)
