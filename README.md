# QA Playbook

Practical templates and checklists for running quality on payment and fintech products. Written from experience leading QA, certification and application support teams.

Copy what you need, adapt it to your team, and keep it versioned next to your code.

## Contents

| Document | Use it when |
|---|---|
| [Test strategy](docs/test-strategy.md) | Starting a product or a major release |
| [Test plan template](templates/test-plan.md) | Planning a specific release or feature |
| [Defect report template](templates/defect-report.md) | Logging a bug that someone else must fix |
| [Root cause analysis](templates/root-cause-analysis.md) | A defect escaped to production or keeps coming back |
| [Release readiness gate](checklists/release-readiness.md) | Deciding whether a build can ship |
| [EMV L3 certification readiness](checklists/emv-l3-certification-readiness.md) | Preparing a terminal or SoftPOS app for scheme certification |
| [POS transaction test matrix](checklists/pos-transaction-matrix.md) | Covering transaction types across card entry modes |
| [Quality metrics](docs/quality-metrics.md) | Reporting quality to engineering and leadership |

## Principles

1. Every test traces to a requirement. Every requirement has at least one test.
2. Find defects as early as possible. A gap found in the SRS is cheaper than a bug found in UAT.
3. Automate checks that run often. Spend human time on exploration and risk.
4. Evidence decides releases. Logs, reports and pass rates, not opinions.
5. Fix the process, not just the bug. Every escaped defect gets a root cause.

## License

MIT
