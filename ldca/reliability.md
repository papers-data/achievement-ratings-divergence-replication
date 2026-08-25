# L-DCA coding reliability — education-individual

**Date:** 2026-06-26. Reproducibility check for the Longitudinal Directed Content
Analysis (L-DCA) of the open-ended evaluation comments.

## Design

The primary coding reported in the paper (Table `tab:ldca`) was performed by a
single human coder who is also the course instructor. To assess whether the
10-code codebook (`codebook.md`) can be applied **reproducibly** — a check on the
coding scheme, not a substitute for independent human coders — the full comment
corpus was re-coded by **two independent automated coders**, blind to each
other and to the primary coding:

- **Coder A:** Claude Opus (Anthropic).
- **Coder B:** DeepSeek-chat (`deepseek-chat`, temperature 0).

Both received the identical codebook and the same comments. Multi-label coding
(0+ of 10 codes per comment) plus one overall valence (positive/negative/mixed).

The corpus was re-extracted from the 14 institutional evaluation PDFs: **157
comments** (Phase 1: 20, Phase 2: 40, Phase 3: 97), reproducing the paper's
n=156 to within one borderline comment.

## Inter-coder agreement (Coder A vs Coder B, n=157)

| Code | Cohen's κ | Agreement | Prev. A | Prev. B |
|------|-----------|-----------|---------|---------|
| METpos | 0.894 | 94.9% | 66 | 58 |
| METneg | 0.745 | 96.8% | 10 | 11 |
| VIDpos | 0.749 | 95.5% | 16 | 15 |
| VIDneg | 0.490 | 97.5% | 2 | 6 |
| ENGpos | 0.342 | 86.0% | 21 | 17 |
| ENGneg | 0.706 | 89.8% | 38 | 32 |
| MOTpos | 0.882 | 94.3% | 94 | 89 |
| MOTneg | 0.553 | 96.2% | 5 | 9 |
| SPA | 1.000 | 100.0% | 14 | 14 |
| AI | 1.000 | 100.0% | 1 | 1 |

- **Mean Cohen's κ (per code): 0.74** — substantial (Landis & Koch).
- **Overall per-decision agreement (10 codes × 157): 95.1%.**
- **Valence κ (3-class): 0.87**; valence agreement 93.0%.

## Reading

Agreement is near-perfect on concrete, low-inference codes (physical-room
conditions and AI references, κ=1.00) and on the high-prevalence methodology and
instructor-praise codes (κ>0.88). It is weakest on the most interpretive code,
improved comprehension/engagement (ENGpos, κ=0.34), and on the two rarest codes
(VIDneg, MOTneg), whose κ is unstable at low prevalence. The automated aggregates
converge with the instructor's primary coding for most codes; the main divergence
is MOTpos, which both automated coders apply more broadly (any instructor praise)
than the instructor's narrower "enthusiasm" definition — a definitional, not a
random, difference.

## Caveat

This is a **codebook-reproducibility** check. It does not remove the deeper
limitation that the primary coder is also the instructor and subject; two
automated coders may also share training biases. A human adjudication of a random
subset would further anchor validity and is left as a low-cost extension.

## Files

- `codebook.md` — the 10-code codebook (identical input to both coders).
- `coding-claude.json`, `coding-deepseek.json` — per-comment codes + valence
  (ids only; verbatim comment text withheld for privacy, available on request).
- Computed with `scikit-learn` `cohen_kappa_score` in the `paper-data` container.
