# Weekly Status Log

Auto-updated by the Sunday Claude routine. Manual notes may be appended between checks.

---

## 2026-06-08 (Cycle 1, day 1) — Manual entry

Plan v4 spec approved. Implementation plan written. Roadmap repo bootstrapping in progress.

Sunday routine not yet configured. First automated entry expected: 2026-06-14 (Sunday of Cycle 1, Week 1).

---

## 2026-06-14 (Cycle 1, week 1 of 2) — Auto check

- Tasks: 2 of 5 done
- Days remaining in cycle: 7
- Outstanding tasks:
  - [ ] Book ISTQB Foundation (CTFL v4.0) exam for Sat 2026-07-18
  - [ ] Save exam confirmation email
  - [ ] Configure scheduled Claude routine — runs Sunday 7 PM, posts status issue here
- Risk: tight — 3 of 5 tasks remain with 7 days left; exam booking requires external action this week.

---

## 2026-06-20 (Cycle 1, week 2 of 2) — Auto check

- Tasks: 3 of 5 done
- Days remaining in cycle: 1
- Outstanding tasks:
  - [ ] Book ISTQB Foundation (CTFL v4.0) exam for Sat 2026-07-18
  - [ ] Save exam confirmation email
- Risk: tight — cycle closes tomorrow with 2 tasks outstanding; both are marked deferred in the cycle file but remain unchecked.

---

## 2026-06-27 (Cycle 2, week 1 of 2) — Auto check

- Tasks: 0 of 5 done
- Days remaining in cycle: 8
- Outstanding tasks:
  - [ ] Read Dosaj study guide Chapters 1–4 (Fundamentals, SDLC, Static, Test Design)
  - [ ] Take 2 mock exams via Guru99 (~30 questions each), record scores
  - [ ] Review wrong answers — write 1 sentence on why each was wrong
  - [ ] Convert one existing Playwright Java test from `inderparhar.dev` repo to Playwright TypeScript
  - [ ] Push the TS test in a new branch on the Website repo
- Risk: slipping — 0 of 5 tasks started with 6 days elapsed; all tasks remain with 8 days left.

---

## 2026-07-07 (Cycle 3, week 1 of 2) — Manual entry

- **ISTQB:** Full syllabus PDF complete (Chapters 1–6). Multiple quizzes taken per section, decent results. Remaining before exam: 1 full timed mock (40q/60min) + final prep this weekend (2026-07-11/12). Exam still booked for Sat 2026-07-18.
- **Pact:** Started learning — contract testing basics (Cycle 2 work-driven carryover, in progress).
- **Playwright:** Started learning basics (Cycle 2 carryover — TS conversion task not yet done).
- Risk: on track for ISTQB — syllabus done ahead of the timed-mock milestone. Watch: first Claude Code skill (Cycle 3 ship) not yet started; Pact + Playwright TS still open from Cycle 2.

---

## 2026-07-07 (Cycle 3) — Manual entry: SDET integration decision

- Added an SDET track to the roadmap (Cycles 4–12), interleaved — QE target unchanged. Design: `docs/2026-07-07-sdet-integration-design.md`.
- **Track A (Python DSA):** continuous from Cycle 4 — repo `python-dsa`, pytest per solution (doubles as whitebox/unit reps). Note: Pact ≠ whitebox/unit; app-repo integration artifact deliberately skipped.
- **Track B (Performance):** one Locust load test in Cycle 6 (extended to 3 weeks).
- **Track C (System Design, test/infra):** study Cycles 8–11, feeds the Cycle 11 interview-prep doc.
- **Timeline:** Cycles 6 and 11 → 3 weeks; plan end moves 2026-11-22 → **2026-12-06**.
- Target: interview-ready for mid/senior SDET **in addition to** QE by schedule end.

---

## 2026-07-12 (Cycle 3, week 1 of 2) — Manual entry: learning-track progress

- **Playwright:** Now learning via LinkedIn Learning "Learning Playwright" course. Past setup/basics — at the **start of writing tests**. Note: this is the JS/TS Playwright, feeds the still-open Cycle 2 TS-conversion carryover.
- **Pact:** Working through the generated decks — currently on **deck 3** of the contract-testing series (work-driven carryover).
- **Java:** Started fundamentals practice on **codingbat.com** (new, self-driven rep work — supports the SDET track / future framework code).
- Risk: on track for ISTQB (exam Sat 2026-07-18). These three are learning-in-progress, not yet tied to shippable Cycle 3 tasks (skill + exam still the cycle deliverables).

---

## 2026-07-28 (Cycle 4, week 2 of 2) — Manual entry / re-baseline

Re-baselined after a two-cycle drift. Root cause: TypeScript sat on the critical path (Playwright-TS carried since Cycle 2) and too many parallel fronts while personal-life events cost time.

- **Cycle 3:** slipped → **grace cycle used** (1 of 2). ISTQB was fully prepped but never booked/sat; first Claude Code skill never started. Both folded forward.
- **ISTQB:** decision — sit it anyway (prep is sunk, marginal cost ~1 fee + 1 hr; it's a filter-passer, not a differentiator). Book earliest seat in Cycle 4. No further study investment.
- **Framework:** switched TS → **Playwright Java** for v0. Java is already known, so v0 ships now; TS port becomes README future-work. Removes the recurring blocker outright.
- **Deferred:** first Claude Code skill → next cycle; **SDET/DSA track → Cycle 5** (was Cycle 4) to stop opening new fronts mid-recovery.
- **Pact:** continue — has a work forcing-function.
- Risk: recoverable. Cycle 4 deliverables (Java framework v0 + booked exam) are both achievable with known tools.

---

## 2026-08-05 (Cycle 5, week 1 of 2) — Manual entry: Playwright Assignment 02 shipped

The Cycle 4 re-baseline worked. Framework v0 + CI are real and green — landed 2026-08-03/05, a few days past the 08-02 due date.

- **Framework:** `assignment-02-todomvc-framework` — 5 Playwright-Java tests vs `demo.playwright.dev/todomvc`, `mvn test` green (5 run / 0 failures / 20.9s). JUnit 5 lifecycle: one browser per class, fresh `BrowserContext` per test (order-independent), headless auto-flipped by the `CI` env var. No `Thread.sleep` anywhere.
- **CI (the new skill):** `test.yaml` — push/PR, ubuntu-latest, JDK 17 temurin + Maven cache, Playwright browser install on the runner, `mvn test`, surefire artifacts uploaded **only** `if: failure()`. Nothing masked with `|| true`.
- **GitHub Actions depth (unplanned bonus):** four more workflows exercised for real — trigger surface incl. cron + `workflow_dispatch` (`lab1`), a 2-OS × 3-Node build matrix (`lab2`), and reusable workflows via `workflow_call` with typed inputs + `secrets: inherit` (`reusable` + `lab3`). This went well past the assignment's ask.
- **Not done — carried to Cycle 5:** no README (so no CI badge, no TS-port note), and the code sits in `Github_Actions1` rather than a public `playwright-java-framework` repo. Two tests use **positional XPath**, and `activeFilterHidesCompletedTodos` never clicks the filter or asserts on it — it is green without testing anything. Fix before layering fixtures on top.
- **ISTQB:** still not booked. Second cycle carrying it.
- Risk: **on track, with a quality caveat.** The blocker that killed Cycles 2–3 (TS on the critical path) is gone and shipping resumed. Watch: a green suite that doesn't assert is worse than a red one — the carryover list is the cost of counting Cycle 4 as shipped.
