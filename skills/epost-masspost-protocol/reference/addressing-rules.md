> **When to use this file:** When validating address format, field lengths, or alignment in the Mailing Request file or physical mail piece.

# Addressing Rules

## Standard Address Structure (Table 9)

| Field | Max Length | Format |
|---|---|---|
| Title / First Name | 40 characters | Optional |
| Last Name | 40 characters | Mandatory |
| Address 1 (House No/Street) | 40 characters | Mandatory |
| Address 2 (Additional Info) | 40 characters | Optional |
| Postcode | 4 characters (numeric) | Mandatory (Belgium) |
| Town | 40 characters | Mandatory |
| Country | 40 characters | Mandatory (if not Belgium) |

## Formatting Guidelines

- All letters must be in **uppercase** (recommended).
- No punctuation (periods, commas, etc.) is allowed in the Town field.
- The Postcode must be separated from the Town by a single space character.
- The Postcode field must be exactly **4 digits** for Belgian addresses.

## Mail Piece Alignment (Table 10)

| Alignment | Specification |
|---|---|
| Left margin | Minimum 15.0 mm |
| Right margin | Minimum 15.0 mm |
| Bottom margin | Minimum 15.0 mm |
| Line spacing | Minimum 1.0 mm |

## Belgian Address Rules

- Belgian addresses must be valid according to the official **bpost postal database**.
- Use the **MailingCheck** action (OptiAddress) to validate addresses before physical distribution.
- For more details on Belgium-specific addressing, see [optiaddress-flows.md](../flows/optiaddress-flows.md).

## Related Files

- For character restrictions, see [character-restrictions.md](./character-restrictions.md)
- For data field specifications, see [../schemas/mailing-request.md](../schemas/mailing-request.md)
