# Statistical analysis — education-individual (Tier-1)

**Date:** 2026-06-24. Computed with SciPy on the project data (`grade-series-2015-2026.csv`,
the 14-semester evaluation series, and per-student finals for 2019-II/2020-II). Reproducible
via `scratchpad/stats.py`.

## Intervention effect (2019-II → 2020-II) — strong and significant

| Outcome | Test | Result |
|---|---|---|
| Final grades (per student) | Welch t, Hedges g | 2.37 (n=35) → 3.73 (n=48); **g = 0.97**, t = 4.22, **p = 8.3e-5** |
| Approval proportion | Cohen's h | 44.7% → 78.2%; **h = 0.71** (medium–large) |
| Perception "Very High" (strategy) | proportion diff + Cohen's h | 25% → 74%; +49% [CI +31,+67]; h = 1.02 |
| Comprehension "Very High" | " | 6% → 65%; +59% [+44,+74]; h = 1.38 |
| Material-use "Low/Very Low" | " | 44% → 4%; −39% [−55,−24]; h = −1.02 |
| Participation "Low/Very Low" | " | 40% → 15%; −24% [−42,−7]; h = −0.56 |

McNemar/Wilcoxon on the paired perception/EME-E shifts require the raw 2020-II pre/post pairs
(in the master's thesis) and are deferred.

## Achievement–satisfaction association — borderline, not a clean causal divergence

- **Per-semester evaluation mean vs approval (n=14): Pearson r = −0.52, p = 0.055, 95% CI [−0.82, +0.01]**
  (Spearman ρ = −0.46, p = 0.10). Negative but not significant at α = 0.05; the CI includes 0.
- **Phase means are not statistically distinguishable** (overlapping 95% CIs):
  P1 4.83 [4.55, 5.12], P2 4.94 [4.82, 5.07], P3 4.60 [4.37, 4.84].

## The post-2022 satisfaction "decline" is weakly identified and confounded

- **Phase-3 trend is endpoint-sensitive:** with 2026-I, OLS slope −0.055/sem, p = 0.29 (Mann-Kendall
  τ = −0.43, p = 0.24) — **not significant**; without 2026-I, −0.132/sem, p = 0.002 (MK τ = −0.87,
  p = 0.017) — significant. The significance of the decline depends on how the rebound is treated.
- **Within each instrument the trend is flat:** Instrument A (2018-I…2023-I, n=9) slope +0.008/sem,
  p = 0.66; Instrument B (2024-I…2026-I, n=5) slope −0.016/sem, p = 0.88. The A→B boundary shows no
  level shift (2023-I 4.71 → 2024-I 4.74, +0.03). The apparent decline lives in the contrast between
  the Phase-2 peak (Instrument A) and the late-B semesters, i.e. it is **confounded with the 2024
  instrument reformulation and scope expansion**, not isolated to the AI era.
- **The clean post-ChatGPT, pre-2024 window** (2022-II → 2023-I, old instrument and old scope) moves
  only −0.16, barely above baseline term-to-term noise (2018-I → 2018-II was −0.06). The AI-only-
  attributable movement is small.
- **Variance increase is real but multiply determined:** F = 20.1 (df 21,38), p = 3e-14 for the
  2025-II vs 2020-II rating variance, but it co-occurs with smaller, lower-turnout samples, the
  instrument change, and the harder content — it cannot be assigned to AI.
- **Non-response does not cleanly explain the decline:** evaluation mean vs response rate r = 0.36,
  p = 0.20 (n=14); within Phase-3 r = 0.16, p = 0.73. Present but not significant.

## Framing implication

- **Defensible spine:** the 2020-II flipped intervention produced large, significant, durable
  achievement gains (g = 0.97; h = 0.71), and recorded approval stayed high (79–100%) for every
  subsequent semester.
- **Defensible (descriptive) dissociation:** the satisfaction proxy did not track those achievement
  gains; the two series are negatively associated (r = −0.52), a within-course illustration of the
  documented SET-validity gap (Deslauriers 2019; Uttl 2017; Gren 2020).
- **Not defensible as causal:** attributing the satisfaction drift to generative AI. It is unmeasured
  (1/156 comments), not significant within either instrument window, endpoint-sensitive, and
  confounded with the 2024 instrument and scope changes. AI must be presented as temporal context and
  one unmeasured hypothesis, not the established cause.
