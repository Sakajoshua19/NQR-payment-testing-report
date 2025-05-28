# NQR Payment Test Cases

| Test Case ID | Description | Expected Result | Actual Result | Status |
|--------------|-------------|------------------|----------------|--------|
| TC001 | Scan valid NQR code | Transaction page loads, payment succeeds | Success | ✅ |
| TC002 | Scan invalid/expired QR code | User sees an error message | Error not shown clearly | ⚠ |
| TC003 | Network timeout during payment | Redirects back to PayXpress with status | User is not redirected, session ends abruptly | ❌ |
| TC004 | Duplicate scan of same QR code | Second transaction blocked or flagged | User is charged twice (duplicate debit) | ❌ |
| TC005 | Attempt payment with unsupported bank | User is informed that their bank is unsupported | No feedback, payment hangs | ⚠ |
| TC006 | UI feedback after scan | User sees transaction status clearly (loading, success, fail) | UI freezes or gives vague messages | ❌ |
