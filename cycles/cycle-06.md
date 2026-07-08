# Cycle 6 — Framework Depth: API + Reporting

**Weeks:** 11–13 (2026-08-17 → 2026-09-06) — extended to 3 weeks for the Track B load-test build
**Status:** pending
**Ship:** API test suite, schema validation, Allure reporting, screenshot/trace on failure.

## Tasks

- [ ] Add 5 API tests against a public auth-bearing API (reqres.in or similar)
- [ ] Schema validation on 3 response bodies
- [ ] Install + configure Allure reporter
- [ ] Configure trace + screenshot on failure
- [ ] README: add "Test Reports" section with screenshot of Allure output
- [ ] **SDET / Track A:** finish DSA fundamentals block (~3/week) in `python-dsa`, pytest + CI green.
- [ ] **SDET / Track B (Performance) — one-shot artifact:** build a Locust load test against the same API this cycle's suite targets; add a README section with a latency/throughput chart.

## Done when

- API tests passing in CI.
- Allure report viewable from a CI artifact link.
- Trace files generated on simulated failure.
