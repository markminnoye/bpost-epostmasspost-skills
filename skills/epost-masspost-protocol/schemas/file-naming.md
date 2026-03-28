> **When to use this file:** When constructing or parsing bpost file names for any request, acknowledgement, or response file transmitted via FTP or e-MassPost.

# File Naming Conventions

Files transmitted to bpost must follow strict naming requirements. This document covers the generic file name format, field descriptions, examples, pre-sorting code file naming, and the `.TMP` extension rule for FTP uploads.

## Generic File Name (XML and TXT)

The file name consists of uppercase fields separated by underscores, terminated by a file extension:

```
AAA_VVVV_CCCCCCCC_NNNNNNNNNN_YYMMDDHHMMSS_SSS.XXX
```

### Field Descriptions

| Field | Description | Rules | Example |
|-------|-------------|-------|---------|
| `AAA` | 3-character alphanumeric code identifying the application | For deposit files: `EMP`. For mailing list files: `MID` | `EMP` |
| `VVVV` | 4-digit version code | Currently `0100` for EMP-files and `0100`, `0102` or `0200` for MID-files | `0100` |
| `CCCCCCCC` | PRS-ID of the PBC of the sender (8 digits max) | Provided by bpost | `ABCD1234` |
| `NNNNNNNNNN` | Customer-assigned 10-character alphanumeric code, uniquely identifying the file | Used for serial number, application code, or internal reference | `56` |
| `YYMMDDHHMMSS` | Timestamp of when the file is generated | | `120214150445` |
| `SSS` | 3-character code identifying the communication step | `0RQ` for Request, `1AK` for Acknowledgement, `2RS` for Response | `0RQ` |
| `XXX` | File extension | Must be uppercase | `XML` |

### Examples

1. **Deposit Request file:**
   ```
   EMP_0100_12345_ABCD123456_120214150334_0RQ.XML
   ```

2. **Corresponding Acknowledgement file:**
   ```
   EMP_0100_12345_ABCD123456_120214150445_1AK.XML
   ```

3. **Corresponding Response file:**
   ```
   EMP_0100_12345_ABCD123456_120214151235_2RS.XML
   ```

## XLS File Naming

With the XLS(X) and CSV file formats, no specific rule is applied on the file naming.

## Pre-sorting Codes File Naming

```
MID_FFFF_PSCVVVVVVV_YYMMDDHHMMSS_3PR.XXX
```

| Field | Description | Rules |
|-------|-------------|-------|
| `FFFF` | Version of the data/structure format | Only format `0100` is supported |
| `VVVVVVV` | Version of the presorting code file | 7 digits (with leading zeros) |
| `YYMMDDHHMMSS` | Timestamp | Same as generic file name |
| `3PR` | Identifies pre-sorting code files | Fixed value |
| `XXX` | File extension | `.TXT` or `.XML` |

### Example

```
MID_0100_PSC0000107_120214143743_3PR.XML
```

## `.TMP` Extension Rule for FTP Uploads

When a file is uploaded using FTP, it can be named with `.TMP` during transmission. This ensures bpost never processes a partial file. Once the upload is completed, the file must be renamed to the appropriate extension.

## Compression (Optional)

The file can be compressed using the Zip algorithm prior to transmission. If compressed, the file name must finish with `.ZIP` (uppercase) after the file format.

---

See [deposit-request.md](deposit-request.md), [mailing-request.md](mailing-request.md), and [presorting-codes.md](presorting-codes.md) for the file structures that use these naming conventions.
