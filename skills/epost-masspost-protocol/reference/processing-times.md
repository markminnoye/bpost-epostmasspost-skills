> **When to use this file:** When planning mailing deadlines, understanding when response files will be ready, or setting expectations for delivery.

# Processing Times

## File Processing Window (Table 12)

| Action | Target Ready Time |
|---|---|
| **Acknowledgement File** | Within 5-15 minutes of upload |
| **Response File** | Within 2-4 hours of upload |
| **Physical Sorting** | Typically same-day for deposits delivered before cutoff |

## System Availability (Table 13)

| Service | Availability |
|---|---|
| e-MassPost Website | 24/7 (except planned maintenance) |
| FTP/FTPS Server | 24/7 (except planned maintenance) |
| Sorting Centers | Monday - Friday (standard business hours) |

## Response Delay Factors

1. **Large File Size**: Files containing >100,000 address records may take longer to process.
2. **System Load**: Peak periods (e.g., end of month, holidays) may introduce additional delays.
3. **Address Quality**: Files with many invalid addresses may require more processing time for validation and error reporting.

## Delivery Deadlines

- Physical deposits must be delivered to bpost **before the specified cutoff time** (usually 16:00) to ensure processing starts on the same day.
- Deposits delivered after the cutoff will be processed on the next business day.

## Related Files

- For sequence diagrams, see [../flows/request-ack-response.md](../flows/request-ack-response.md)
- For onboarding info, see [onboarding.md](./onboarding.md)
