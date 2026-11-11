# POS Transaction Test Matrix

Cover each transaction type against each entry mode. Mark N/A where the scheme or product does not allow the combination.

## Coverage matrix

| Transaction | Chip | Contactless | Mag stripe | Fallback | Manual |
|---|---|---|---|---|---|
| Sale | | | | | |
| Sale with cashback | | | | | N/A |
| Refund | | | | | |
| Void | | | | | |
| Reversal (timeout) | | | | | |
| Pre-auth | | | | | |
| Pre-auth completion | | | | | |
| Tip adjustment | | | | | |
| Balance enquiry | | | | | N/A |

## Scenarios per cell

For each combination, run at least:

1. Approved online
2. Declined by issuer
3. Wrong PIN, then correct PIN
4. Host timeout, reversal sent
5. Card removed early (chip)
6. Amount at limit boundaries (floor limit, CVM limit, contactless limit)

## Cross-cutting checks

- [ ] Receipt content and masking
- [ ] Transaction log entry on terminal and host
- [ ] STAN increments, RRN unique
- [ ] Batch totals match after each transaction
- [ ] Duplicate request handled idempotently
- [ ] Power loss mid transaction recovers correctly
