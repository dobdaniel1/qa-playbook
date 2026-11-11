# Quality Metrics

Track a small set of metrics that drive decisions. Report trends, not single numbers.

| Metric | Formula | Healthy signal |
|---|---|---|
| Requirement coverage | Requirements with at least one test / total requirements | 100% for in-scope items |
| Test pass rate | Passed / executed | Rising through the cycle, 95%+ at release |
| Defect escape rate | Production defects / total defects found | Falling release over release |
| Defect removal efficiency | Defects found before release / total defects | 90%+ |
| Mean time to resolve | Average time from defect open to verified fix | Stable or falling |
| Automation coverage | Automated regression cases / total regression cases | Rising |
| Flaky test rate | Tests with inconsistent results / automated tests | Under 2% |
| Reopen rate | Reopened defects / fixed defects | Under 5% |
| Certification first-pass rate | Scheme test cases passed first run / total | Rising |
| Transaction success rate (prod) | Approved or correctly declined / total attempts | Matches baseline |

## Reporting tips

- Pair every metric with the decision it supports.
- Show severity breakdowns. Ten cosmetic bugs are not one critical bug.
- Call out blockers and risks in plain words at the top.
