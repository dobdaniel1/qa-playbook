# Test Strategy

A test strategy sets how a product is tested over its life. A test plan applies it to one release.

## 1. Scope

- **Product:** name, version, channels (POS, SoftPOS, mobile, web, API).
- **In scope:** features, integrations, platforms and devices.
- **Out of scope:** what is not tested, and who owns it instead.

## 2. Quality risks

List what would hurt most if it failed. Rank by impact and likelihood.

| Risk | Impact | Likelihood | Mitigation |
|---|---|---|---|
| Customer debited but transaction marked failed | High | Medium | Reversal and reconciliation tests on every release |
| Wrong host routing for a BIN range | High | Low | Routing table tests, BIN boundary cases |
| Timeout handling differs from scheme rules | High | Medium | Timeout and late response scenarios |
| Settlement file mismatch | High | Medium | Automated file comparison against ledger |

## 3. Test levels

| Level | Owner | Tooling | Runs |
|---|---|---|---|
| Unit | Developers | Pytest, JUnit | Every commit |
| Contract and API | QA and developers | Karate, Pytest | Every pull request |
| Integration | QA | Karate, Docker Compose | Every merge to main |
| End to end UI | QA | Playwright | Nightly and pre-release |
| Performance | QA | k6, JMeter | Before major releases |
| Security | QA and security | OWASP ZAP, dependency scans | Weekly and pre-release |
| Certification | Certification team | Scheme and lab tools | Per scheme requirement |
| UAT | Business owners | Manual, guided scripts | Pre-release |

## 4. Test types for payments

- **Functional:** sale, refund, void, reversal, cashback, pre-auth and completion, balance enquiry.
- **Entry modes:** chip, contactless, magnetic stripe, fallback, manual entry.
- **Negative:** declined, insufficient funds, wrong PIN, expired card, blocked card, invalid amount.
- **Resilience:** host timeout, host down with failover, duplicate request, network drop mid transaction.
- **Data integrity:** amounts, currency codes, STAN and RRN uniqueness, ledger balance after reversal.
- **Settlement:** end of day batch, file format, totals, duplicate and partial records.

## 5. Environments and data

- Separate environments for dev, QA, staging and certification.
- Use scheme test cards and synthetic data only. Never production card data.
- Seed data is scripted and repeatable.

## 6. Entry and exit criteria

**Entry:** requirements approved, build deployed, smoke tests pass, test data ready.

**Exit:** see the [release readiness gate](../checklists/release-readiness.md).

## 7. Defect management

- Severity is impact. Priority is urgency. Record both.
- Every defect has steps, expected result, actual result and evidence.
- Escaped defects get a [root cause analysis](../templates/root-cause-analysis.md).

## 8. Reporting

Daily: execution progress and blockers. Per release: the metrics in [quality metrics](quality-metrics.md).
