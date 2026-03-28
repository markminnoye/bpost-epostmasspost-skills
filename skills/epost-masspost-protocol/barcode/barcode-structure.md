> **When to use this file:** When building the barcode data string, choosing the correct FCC for your product, or validating a 16-digit Mail ID barcode value.

# Barcode Structure

The Mail ID barcode identifies each mail piece individually. It is a **16-digit numeric string**.

## 16-Digit Barcode Format

```
Digits 1-2:   FCC (Format Control Code)
Digits 3-10:  Customer ID (assigned by bpost)
Digits 11-16: Mail Piece Number (sequential)
```

**Example:** `0100456123456789`
- `01` - Format Control Code
- `00456123` - Customer ID
- `456789` - Mail Piece Number

## Format Control Code (FCC)

The FCC identifies the type of mail being sent. The most common FCCs are:

| FCC | Description | Product |
|---|---|---|
| `01` | Non-sorted mail | Mail ID |
| `02` | Sorted mail (R&S) | Round & Sequence |
| `03` | OptiAddress | OptiAddress |
| `07` | Registered mail | Registered |

## Customer ID

- 8-digit identifier assigned by bpost to the customer during onboarding.
- This ID remains the same for all mail pieces from the same customer.
- If your assigned ID is shorter than 8 digits, pad with leading zeros.

## Mail Piece Number

- 6-digit numeric string (000001 to 999999).
- Must be **unique** within the same deposit and within a 6-month period for the same Customer ID.
- Sequential numbering is recommended (000001, 000002, etc.).

## Barcode String Encoding

- The 16-digit string is encoded using the **Code 128** symbology (Subset C).
- For encoding details, see [code128-encoding.md](./code128-encoding.md).

## Related Files

- For printing requirements, see [barcode-printing.md](./barcode-printing.md)
- For encoding steps, see [code128-encoding.md](./code128-encoding.md)
