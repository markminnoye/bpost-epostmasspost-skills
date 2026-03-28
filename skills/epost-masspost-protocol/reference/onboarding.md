> **When to use this file:** When starting a new integration project, registering for a Customer ID, or setting up FTP credentials.

# Onboarding Process

## Step 1: Registration

1. Contact bpost via **customer.operations@bpost.be** to express interest in MAIL ID or R&S.
2. Provide your company details and estimated mailing volume.
3. Reference your existing bpost account number if applicable.

## Step 2: Customer ID Assignment

- bpost will assign a unique **8-digit Customer ID**.
- This ID must be used in all barcodes and file headers.
- For more details, see [../barcode/barcode-structure.md](../barcode/barcode-structure.md).

## Step 3: Account Credentials

- bpost will provide credentials for:
  - **e-MassPost website** (HTTP interactive mode)
  - **FTP/FTPS server** (Unattended mode)
- Ensure your technical team has these credentials securely stored.

## Step 4: Technical Validation

1. Develop your integration using the provided documentation.
2. Submit a **test deposit** (XML or TXT) via the e-MassPost website.
3. Verify that you receive an Acknowledgement and a Response file without errors.
4. (R&S only): Perform a physical sample verification with bpost to ensure sequence references are printed correctly.

## Step 5: Go-Live

- Once test deposits are successful, you are authorized to send production deposits to the MAIL ID system.

## Support Contact

- **Technical Support**: customer.operations@bpost.be
- **Website**: [www.bpost.be/emasspost](https://www.bpost.be/emasspost)

## Related Files

- For file naming rules, see [../schemas/file-naming.md](../schemas/file-naming.md)
- For connection details, see [../transport/ftp-protocol.md](../transport/ftp-protocol.md)
