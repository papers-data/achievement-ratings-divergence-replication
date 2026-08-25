# FLP Longitudinal Grade Outcomes, 2015-II – 2026-I

**Prepared:** 2026-06-24
**Course:** 750095M *Fundamentos de Lenguajes de Programación* (2015–2023) /
750017C *Fundamentos de Interpretación y Compilación de Lenguajes de Programación* (2024–2026)
**Instructor:** Carlos A. Delgado S. — Universidad del Valle, sede Tuluá
**Method:** Final grades extracted from each semester's authoritative gradebook (instructor
*Consolidado* `Nota`/`Definitiva` column for 2015–2022; SIRA *Total del curso (Real)* export for
2023–2026), computed exactly with Python and independently re-verified by an adversarial recount
(36 agents, one extractor + one verifier per semester). Colombian 0.0–5.0 scale; approval ≥ 3.0.

---

## 1. Master series

| Semester | Enrolled | Finished | Approved | Failed | Withdrew | Pass% (enr.) | Mean final | Source |
|----------|:---:|:---:|:---:|:---:|:---:|:---:|:---:|---|
| 2015-II | 48 | 33 | 27 | 6 | 15 | 56.2 | 3.95 | consolidado |
| 2016-II | 25 | 25 | 24 | 1 | 0 | 96.0 | 3.78 | consolidado |
| 2017-I  | 25 | 20 | 11 | 9 | 5 | 44.0 | 2.85 | roster+consolidado |
| 2018-I  | 32 | 32 | 25 | 7 | 0 | 78.1 | 3.31 | consolidado |
| 2018-II | 32 | 32 | 23 | 9 | 0 | 71.9 | 3.39 | consolidado |
| 2019-I  | 29 | 28 | 20 | 8 | 1 | 69.0 | 3.38 | consolidado |
| **2019-II** | **38** | **35** | **17** | **18** | **3** | **44.7** | **2.37** | roster+consolidado |
| 2020-I  | 28 | 28 | 27 | 1 | 0 | 96.4 | 3.94 | consolidado |
| **2020-II** | **55** | **48** | **43** | **5** | **7** | **78.2** | **3.73** | consolidado *(intervention)* |
| 2021-II | 51 | 43 | 37 | 6 | 8 | 72.5 | 3.50 | roster+consolidado |
| 2022-I  | 35 | 35 | 35 | 0 | 0 | 100.0 | 4.17 | consolidado |
| 2022-II | 38 | 38 | 30 | 8 | 0 | 79.0 | 3.43 | consolidado |
| 2023-I  | 45 | 45 | 39 | 6 | 0 | 86.7 | 3.68 | SIRA |
| 2024-I  | 66 | 66 | 62 | 4 | 0 | 93.9 | 3.68 | SIRA (Filen) |
| 2024-II | 30 | 30 | 30 | 0 | 0 | 100.0 | 4.18 | SIRA |
| 2025-I  | 31 | 31 | 29 | 2 | 0 | 93.5 | 3.87 | SIRA (Filen) |
| 2025-II | 47 | 47 | 45 | 2 | 0 | 95.7 | 3.60 | SIRA |
| **2026-I** | **75** | **75** | **74** | **1** | **0** | **98.7** | **3.88** | SIRA *(G50 + G51)* |

Pass% (enr.) = approved / enrolled. For SIRA-export and most consolidado semesters, formally
cancelled students are already absent from the gradebook, so `withdrew` is a floor, not an exact
count (see §4).

---

## 2. The headline finding: achievement rose while satisfaction fell

Aggregating by the paper's three analytical phases:

| Phase | Grade pass rate (enrolled-weighted) | Mean final grade | Institutional evaluation mean (satisfaction) |
|---|:---:|:---:|:---:|
| **1 — Baseline** (2015-II … 2019-II) | **64.2 %** (volatile 44–96) | 3.29 | 4.83 |
| **2 — Intervention** (2020-I … 2021-II) | **79.9 %** | 3.72 | 4.94 |
| **3 — AI era** (2022-I … 2026-I, all 8) | **93.7 %** | 3.81 | 4.57 → 4.82 (2026-I rebound) |

**Grade outcomes and satisfaction diverge after 2022.** Course evaluation means fell from the
5.00 peak (2020-II) to a 4.24 trough (2025-II) — the decline the current paper attributes to the
generative-AI era. **Pass rates did the opposite: they climbed and stayed high (79–100 %)
throughout the same AI-era window**, never returning to the volatile 44–96 % of the
pre-intervention baseline. Mean final grades show the same monotone rise (3.29 → 3.72 → 3.82).

This is the most important new result. It means the post-2022 decline is a **satisfaction /
perception** phenomenon, **not an achievement** phenomenon — exactly the performance-vs-rating
dissociation the paper already cites from Gren (2020), now demonstrated within a single course
across eleven years, and consistent with Kosar et al. (2024), who found no significant effect of
permitted ChatGPT use on grades. The flipped intervention's achievement benefit was **durable**;
what eroded was how students *rated* the methodology, not whether they passed.

---

## 3. Reconciliation with the thesis and the evaluation series

The grade ground truth resolves three numbers the current paper inherits from secondary sources.

- **2019-II diagnostic cohort.** The paper (via the master thesis) cites 48 enrolled / 45.83 %
  approved / 33.34 % failed / 20.83 % withdrew. The actual 2019-II grade roster is 38 enrolled,
  17 approved (**44.7 %**), 18 failed, 3 no-grade. The **pass rate matches the thesis headline
  (~45 %)**, validating the diagnostic claim, but the enrolled base (38 vs 48) and the
  failed/withdrew split differ — the thesis figure aggregates a differently-defined cohort. The
  institutional evaluation's "18 matriculados" for 2019-II is a transcription artifact (18 = the
  failure count); the roster is 38.

- **2020-II intervention cohort.** The paper cites 55 enrolled / 85.47 % approved / 1.81 % failed /
  12.72 % withdrew (official acta, post-*habilitación*). The raw instructor gradebook, under a
  strict ≥ 3.0 rule, shows 43 approved / 5 failed / 7 withdrew of 48 graded (**78.2 %** of 55).
  Both tell the same story — a near-doubling of the pass rate from 2019-II's ~45 % — but the
  thesis's 85 %/1.8 % reflects the official acta reclassifying near-zero abandoners (who still carry
  a low grade in the working sheet) as *withdrawn* and crediting *habilitación* make-up exams. The
  honest, reproducible figure is "pass rate roughly doubled, 45 % → 78–85 %."

- **Enrollment drift.** Institutional-evaluation "matriculados" frequently undercounts the grade
  roster (2019-II 18 vs 38; 2020-II 45 vs 55; 2024-I 56 vs 66), reflecting the regional campus
  capturing the count at different times. Grade rosters are the more reliable enrollment base.

---

## 4. Data-quality notes and caveats

1. **Withdrawals are a floor, not exact.** Formally cancelled students are removed from most
   gradebooks before grading, so `withdrew` is computed as `enrolled − finished`. The 2021-II
   audit is the cautionary case: its SRA roster carries 8 *un-numbered* cancelled students absent
   from the consolidado, raising enrolled from 43 to **51** and withdrew from 0 to 8. Other
   semesters with `withdrew = 0` (where enrolled was taken equal to finished) may similarly
   undercount cancellations.

2. **"Pre-habilitación" raw rule.** Counts use the instructor's computed final ≥ 3.0. The official
   acta can be 1–5 points more generous per semester (*habilitación* make-ups, late-delivery
   equivalences, near-zero abandoners reclassified as withdrawn). Applied **consistently across all
   18 semesters**, the raw rule yields a comparable series; absolute pass rates are conservative.

3. **Series now complete (18/18).** 2024-I and 2025-I, initially absent from the local archive,
   were recovered from the Filen file service (`/Flp`) as SIRA *Calificaciones* exports and yield
   93.9 % and 93.5 % pass rates — fully consistent with the AI-era band. No grade semester remains
   missing.

4. **2026-I is two parallel groups.** G50 (38 students, 100 % pass, mean 3.93) and G51 (37 students,
   36 approved / 1 fail at 2.7, mean 3.82). This is the first semester with a parallel section — a
   structural change from the single-section framing in the current manuscript. Only G51 has an
   institutional evaluation (mean 4.82, 30 % response); G50 was not evaluated.

---

## 5. Implications for the manuscript

1. **Add a longitudinal grade series** (this table) as a second backbone alongside the evaluation
   series. The paper currently rests grades on a single 2019-II-vs-2020-II before/after pair; the
   full 2015–2026 series is far stronger and is the natural complement to the 14-semester
   satisfaction curve.

2. **Reframe Phase 3** from "decline" to "**a satisfaction decline without an achievement
   decline**." This is more defensible, more interesting, and turns a potential reviewer objection
   ("are students actually worse off?") into a finding. It directly operationalizes the Gren (2020)
   dissociation and corroborates Kosar et al. (2024).

3. **Incorporate 2026-I as a partial rebound** in both grades (98.7 % pass) and satisfaction (G51
   mean 4.82, up from 4.24) — explicitly hedged by the 30 % response rate, the single evaluated
   group, and the persistent physical-room (SPA) complaint.

4. **Soften the 2020-II grade figures** to the reproducible "pass rate ~doubled (45 % → ~80 %)",
   citing the official-acta vs raw-gradebook distinction, rather than leaning on the precise
   85.47 %/1.81 % the raw data cannot reproduce.

5. **Title/scope:** the series now spans 2015–2026 (grades) and 2018–2026 (evaluations). "Seven-year"
   is no longer accurate; consider "An Eleven-Year Grade and Evaluation Record" or scope the claim
   to the evaluation window explicitly.
