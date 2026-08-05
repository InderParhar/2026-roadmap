# Cycle 5 — Framework Depth: Fixtures + Config

**Weeks:** 9–10 (2026-08-03 → 2026-08-16)
**Status:** in progress (started 2026-08-03)
**Ship:** Custom fixtures, env config (dotenv), soft assertions, README "Architecture Decisions" section.

> **Note (2026-08-05):** Cycle 4's framework + CI landed 1–3 days into this cycle. Do the carryover below **first** — fixtures and config on top of a repo with no README and two weak tests is building on sand.

## Carryover from Cycle 4 (do first)

- [ ] Extract the framework into public `playwright-java-framework` (MIT) — currently inside `Github_Actions1`
- [ ] README v1: what it tests, how to run, architecture sketch, CI badge, "TS port — future work"
- [ ] Kill positional XPath in `clearCompletedRemovesOnlyCompletedTodos` + `activeFilterHidesCompletedTodos`
- [ ] Fix `activeFilterHidesCompletedTodos` (green but asserts nothing about the filter) and add test 4's missing post-clear assertion
- [ ] Prove CI can fail: deliberate red push, confirm surefire artifacts upload

## Tasks

- [ ] Add 2 custom Playwright fixtures (authenticated user, pre-loaded test state)
- [ ] Read base URL + credentials from `.env` — never hardcode
- [ ] Refactor 3 tests to use soft assertions
- [ ] README: add "Architecture Decisions" section — 3 decisions with the WHY
- [ ] **SDET / Track A:** ~3 problems/week (two-pointer, sorting/searching) in `python-dsa`, each with pytest, CI green.

## Done when

- Fixtures in use across at least 2 tests.
- `.env.example` present, real `.env` gitignored.
- Architecture Decisions section written and pushed.
