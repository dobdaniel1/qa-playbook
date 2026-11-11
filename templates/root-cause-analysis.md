# Root Cause Analysis

Use for escaped defects, production incidents and defects that keep coming back. The goal is to fix the process, not to blame a person.

| Field | Value |
|---|---|
| Incident or defect ID | |
| Date detected | |
| Detected by | Customer / Monitoring / QA / Support |
| Impact | Customers, transactions, amount, duration |
| Severity | |

## 1. What happened

Short timeline from first occurrence to resolution.

| Time | Event |
|---|---|
| | |

## 2. Five whys

1. Why did the failure happen?
2. Why?
3. Why?
4. Why?
5. Why? (root cause)

## 3. Root cause category

- [ ] Requirement missing or unclear
- [ ] Design gap
- [ ] Code defect
- [ ] Configuration or environment
- [ ] Test gap (case missing)
- [ ] Test gap (case existed but was not run)
- [ ] Third party or upstream change
- [ ] Deployment or release process

## 4. Why testing did not catch it

Be specific. Name the missing test, environment difference or skipped step.

## 5. Actions

| Action | Type | Owner | Due | Status |
|---|---|---|---|---|
| Fix the defect | Correct | | | |
| Add regression test | Prevent | | | |
| Update requirement or checklist | Prevent | | | |
| Add monitoring or alert | Detect | | | |

## 6. Follow-up

Date to confirm the actions worked.
