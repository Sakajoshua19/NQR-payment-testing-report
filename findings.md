# Key Issues & Observations

## ❗ Major Bugs

1. *Duplicate Debit*
   - Scanning the same QR code twice within a short window can cause the user to be debited multiple times.
   - No transaction check logic appears to be in place.

2. *Session Timeout Handling*
   - If a transaction times out (e.g., user takes too long to pay), the session ends silently.
   - No redirection to PayXpress or status feedback is given.

3. *UI Feedback Failure*
   - During scanning and transaction flow, status indicators are unclear or absent.
   - This causes confusion for users about whether a payment succeeded or failed.

## ⚠ Minor Issues

- *Unsupported Banks Not Flagged*
  - When using banks not supported by NIBSS, the system doesn’t inform users — it just hangs.
- *No reconciliation confirmation*
  - After successful payment, reconciliation message isn’t always delivered or confirmed in logs.
