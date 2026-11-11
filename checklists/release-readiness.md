# Release Readiness Gate

A build ships when every required item is checked or has a signed-off exception.

## Testing

- [ ] All in-scope requirements traced to executed tests
- [ ] Pass rate at or above agreed threshold (default 95%)
- [ ] No open Critical defects
- [ ] No open High defects without an approved workaround
- [ ] Full regression suite run on the release build
- [ ] Smoke tests pass on staging with production-like config
- [ ] Performance results within agreed limits (latency, throughput, error rate)
- [ ] Security scan run, no unresolved high findings

## Payments specific

- [ ] Reversal and timeout flows tested end to end
- [ ] Settlement file generated and reconciled against ledger
- [ ] Routing and BIN tables match approved config
- [ ] Scheme certification still valid for kernel and app version
- [ ] Card data masked in all logs and receipts

## Operations

- [ ] Release notes written
- [ ] Rollback plan written and tested
- [ ] Monitoring and alerts in place for new features
- [ ] Support team briefed, known issues documented
- [ ] Device configuration and parameter files versioned

## Sign-off

| Role | Name | Go / No go | Date |
|---|---|---|---|
| QA lead | | | |
| Engineering lead | | | |
| Product owner | | | |

## Exceptions

| Item | Reason | Risk accepted by | Date |
|---|---|---|---|
| | | | |
