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

## 2026-07-04 (Cycle 2, week 2 of 2) — Auto check

- Tasks: 4 of 7 done
- Days remaining in cycle: 1
- Outstanding tasks:
  - [ ] Convert one existing Playwright Java test from `inderparhar.dev` repo to Playwright TypeScript
  - [ ] Push the TS test in a new branch on the Website repo
  - [ ] Learn Pact for contract testing (consumer-driven contracts) — added for a work reason
- Risk: slipping — cycle closes tomorrow with 3 of 7 tasks outstanding; Playwright TS conversion and Pact learning are unlikely to complete in 1 day.

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

## 2026-07-11 (Cycle 3, week 1 of 2) — Auto check

- Tasks: 1 of 6 done
- Days remaining in cycle: 8
- Outstanding tasks:
  - [ ] 1 full timed mock exam (40 questions / 60 min), score ≥ 75%
  - [ ] Sat 2026-07-18: sit ISTQB exam
  - [ ] On pass: add cert badge to LinkedIn
  - [ ] Build + publish first Claude Code skill (`playwright-test-from-jira`)
  - [ ] Skill ships as: public GitHub repo with README, example input/output, install instructions
- Risk: tight — exam is 7 days away and the first skill has not been started; both the timed mock and the full skill build must complete within this cycle.

---

## 2026-07-18 (Cycle 3, week 2 of 2) — Auto check

- Tasks: 1 of 6 done
- Days remaining in cycle: 1
- Outstanding tasks:
  - [ ] 1 full timed mock exam (40 questions / 60 min), score ≥ 75%
  - [ ] Sat 2026-07-18: sit ISTQB exam
  - [ ] On pass: add cert badge to LinkedIn
  - [ ] Build + publish first Claude Code skill (`playwright-test-from-jira`)
  - [ ] Skill ships as: public GitHub repo with README, example input/output, install instructions
- Risk: slipping — cycle closes tomorrow with 5 of 6 tasks outstanding; the Claude Code skill has not been started.

---

## 2026-07-25 (Cycle 4, week 1 of 2) — Auto check

- Tasks: 0 of 7 done
- Days remaining in cycle: 8
- Outstanding tasks:
  - [ ] New repo: `playwright-ts-framework` (public, MIT)
  - [ ] Skeleton: `playwright.config.ts`, 5 passing tests against a public demo target (e.g. `demo.playwright.dev/todomvc`)
  - [ ] GitHub Actions CI green on every push
  - [ ] README v1: what it tests, how to run, architecture sketch
  - [ ] Draft Sagacity PoC proposal: which area to PoC, time-box, success criteria
  - [ ] Send proposal to team / manager — get a yes/no/discuss reply
  - [ ] **SDET / Track A (DSA) — starts:** create public repo `python-dsa` (MIT, GitHub Actions CI). ~3 problems/week (arrays/strings, hashmaps) — one pytest test per solution, CI green.
- Risk: slipping — 0 of 7 tasks started with 5 days elapsed; the PoC proposal requires an external reply before that task can close, and 8 days remain.
