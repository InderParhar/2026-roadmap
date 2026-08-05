# Cycle 4 — Framework Skeleton (Java) + Book ISTQB

**Weeks:** 7–8 (2026-07-20 → 2026-08-02)
**Status:** core ship landed — **late (2026-08-03/05, past the 08-02 due date)**, with carryover
**Ship:** Playwright **Java** framework v0 in a new public repo; ISTQB exam booked (sunk prep → sat seat).

> **Re-baseline note (2026-07-28):** Cycle 3 slipped for personal reasons — grace cycle used, folded forward into here. Framework switched from TypeScript to **Playwright Java**: TS-on-the-critical-path was the recurring blocker (carried since Cycle 2), and Java is already known, so v0 ships now and the TS port becomes future work. SDET/DSA track **deferred to Cycle 5** to stop opening new fronts while catching up.

> **Delivery note (2026-08-05):** Framework + CI built as `assignment-02-todomvc-framework` (Playwright track), pushed to **`InderParhar/Github_Actions1`**. 5 tests green locally (`mvn test` — 5 run, 0 failures, 20.9s) and a real Java Playwright workflow runs on GitHub. Two acceptance criteria are **not** met yet: no README, and the public `playwright-java-framework` repo doesn't exist. Two tests also need locator/assertion fixes before this is a defensible portfolio piece — see Carryover.

## Tasks

- [ ] **Book ISTQB Foundation exam** — earliest available seat. Prep is already complete (full syllabus + mocks); this is a booking action, not a study task. Save confirmation email.
- [ ] New repo: `playwright-java-framework` (public, MIT) — _code exists but lives in `Github_Actions1` (the GH-Actions learning repo). Needs extracting into its own named public repo._
- [X] Skeleton: `pom.xml` (Playwright for Java `com.microsoft.playwright`), 5 passing tests against a public demo target — **done:** `com.inder.todomvc.TodoMvcTest`, 5/5 green vs `demo.playwright.dev/todomvc`. JUnit 5 lifecycle: one browser per class, fresh `BrowserContext` per test (order-independent), headless flipped by the `CI` env var.
- [ ] Stable locators only — `getByRole` → `getByText` → `getByLabel` → `getByTestId`. No positional XPath, no `Thread.sleep` (auto-wait). — _`Thread.sleep`: clean, none. **Positional XPath present** in `clearCompletedRemovesOnlyCompletedTodos` and `activeFilterHidesCompletedTodos`. Not done._
- [X] GitHub Actions CI green on every push (headless, artifacts on failure) — **done:** `.github/workflows/test.yaml` — push + PR triggers, `ubuntu-latest`, `setup-java@v4` JDK 17 temurin with Maven cache, Playwright browser install via `exec:java … CLI install --with-deps`, `mvn test`, `upload-artifact@v4` of `target/surefire-reports/**` guarded by `if: failure()`. Nothing `|| true`'d, so a test failure still fails the job.
- [ ] README v1: what it tests, how to run, architecture sketch, **"TS port — future work"** note — _not started; no README in the repo, so no CI badge either._
- [ ] **Pact (work-driven):** finish contract-testing basics — has a work forcing-function, don't let it drift

## Also done (not planned — GitHub Actions depth)

Went past the single CI file into the mechanics of Actions itself. Four extra workflows, all pushed and run:

- `lab1.yaml` — trigger surface: `push`, `pull_request`, `schedule` (nightly cron), `workflow_dispatch`.
- `lab2.yaml` — build matrix: 2 OS × 3 Node versions = 6 parallel jobs.
- `reusable.yaml` + `lab3.yml` — reusable workflows: `workflow_call` with typed inputs and `secrets: inherit`, called by a caller workflow.

This is the "thing you have never done in Java — CI" goal met with room to spare; it's the strongest part of the cycle.

## Carryover into Cycle 5

- [ ] Create public `playwright-java-framework` repo (MIT) and move the framework out of `Github_Actions1`.
- [ ] README v1 + CI badge + "TS port — future work" note.
- [ ] Replace positional XPath with role/testid locators in tests 4 and 5.
- [ ] Fix `activeFilterHidesCompletedTodos` — it builds an "Active" filter locator but never clicks it and never asserts, so it is green without testing the filter. Also add the missing post-`Clear completed` assertion in test 4.
- [ ] Re-verify: `mvn test` 3× clean, then a deliberate red push to prove CI fails and uploads artifacts.

## Deferred out of this cycle

- **First Claude Code skill** (`playwright-test-from-jira`) → next cycle; downstream of the framework anyway.
- **SDET / Track A (DSA)** → starts Cycle 5. Not opened here to avoid a fifth parallel front while re-baselining.

## Done when

- `playwright-java-framework` repo public with CI badge green, README demonstrates run + architecture.
- ISTQB seat booked with confirmation saved.

_Status against this bar (2026-08-05): tests + CI green, repo/README/badge outstanding, exam not booked._
