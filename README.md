# Diverging Achievement and Student Ratings: Replication Package

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22102422.svg)](https://doi.org/10.5281/zenodo.22102422)
[![Code: MIT](https://img.shields.io/badge/code-MIT-blue.svg)](LICENSE)
[![Data: CC BY 4.0](https://img.shields.io/badge/data-CC%20BY%204.0-lightgrey.svg)](LICENSE)

Data, coding materials, and analysis behind *Diverging Achievement and Student
Ratings in an Introductory Programming Course: An Eleven-Year Longitudinal Case
Study*.

Nothing in this package identifies a student.

## What is in it

```
data/       the two longitudinal series, as CSV
ldca/       the content-analysis codebook and the two independent codings
scripts/    the segmented interrupted-time-series analysis
results/    the reports that produce the article's tables
```

### `data/`

One course at the Tuluá campus of Universidad del Valle, followed across
eleven years. The course changed code partway through, from 750095M
*Fundamentos de Lenguajes de Programación* to 750017C *Fundamentos de
Interpretación y Compilación de Lenguajes de Programación*, and the same
instructor taught every offering.

| File | Rows | Contents |
|---|--:|---|
| `grade-series-2015-2026.csv` | 18 | one row per offering: enrolled, finished, approved, failed, withdrawn, pass rates on both denominators, mean final grade, the record it came from, and a confidence flag |
| `evaluation-series-2018-2026.csv` | 14 | one row per offering with an institutional evaluation: segment, mean, standard deviation, and response rate on a 5-point scale |

The two series do not cover the same semesters. Grades run from 2015-II to
2026-I; institutional evaluations begin in 2018-I, because the campus did not
issue them earlier for this course. Neither series is continuous: the course was
not offered in 2016-I, 2017-II, 2021-I, or 2023-II, among others. The analysis
script treats those as missing time rather than closing the gap, which matters
for any time-series model fitted to these data.

**Two denominators, two pass rates.** `pass_rate_enrolled` divides by everyone
on the initial roster; `pass_rate_finished` divides by those who reached the
final grade. Withdrawal rates vary sharply across the series, so the two
diverge by more than 25 points in 2015-II alone. The article reports the
enrolled denominator throughout. Check which one a downstream analysis needs
before using either.

**`confidence` and `notes` are not decoration.** Early semesters were
reconstructed from more than one institutional record, and where those records
disagree the `notes` column says so. 2017-I is the clearest case: the
instructor's own acta narrative claims 16 approved, while applying the
harmonized rule of a final grade at or above 3.0 gives 11. The series uses the
harmonized rule everywhere, and the discrepancy is recorded rather than
smoothed away.

### `ldca/`

Open-ended comments from the fourteen institutional evaluations, coded under
Longitudinal Directed Content Analysis with a 10-code scheme (8 codes set in
advance, 2 added inductively).

| File | Contents |
|---|---|
| `codebook.md` | the 10 codes with their inclusion rules, plus the overall-valence rule |
| `coding-claude.json`, `coding-deepseek.json` | per-comment codes and valence from two automated coders working independently and blind to each other |
| `reliability.md` | the reliability design and its results: per-code Cohen's kappa, valence kappa, per-decision agreement |

**The verbatim comments are not here, and the coders were not human.** Comments
appear only as opaque identifiers (`C001`, `C002`, ...). The primary coding
reported in the article was done by a single human coder who is also the course
instructor; the two automated codings in this folder test whether the codebook
can be applied reproducibly. That is a check on the coding scheme, not a
substitute for independent human coders, and `reliability.md` says so at
length. Read it before treating the kappas as inter-rater agreement in the
usual sense.

### `scripts/`

`its_analysis.py` fits the segmented interrupted-time-series models on the
grade series. It places semesters on a half-year index so that gaps in the
offering history stay open, splits the record into a baseline (2015-II to
2019-II), two separately dummied pandemic semesters (2020-I under emergency
remote teaching, 2020-II the flipped intervention), and a sustained era
(2021-II to 2026-I), and reports the level and trend changes with a
Newey-West sensitivity check.

Requires Python 3 with NumPy, pandas, SciPy, and statsmodels. It resolves its
own paths, so it runs from anywhere:

```bash
python3 scripts/its_analysis.py
```

It reads `data/grade-series-2015-2026.csv` and overwrites
`results/its-analysis.md`. Running it on a clean checkout reproduces the shipped
report byte for byte.

### `results/`

| File | Contents |
|---|---|
| `longitudinal-grades-report.md` | how each semester's figures were extracted and verified, semester by semester |
| `its-analysis.md` | output of `its_analysis.py`: segment descriptives, model coefficients, sensitivity checks |
| `statistical-analysis.md` | the 2019-II to 2020-II intervention comparison and the divergence tests |

## What is not here

The per-student grade records and the verbatim comment corpus. Both stay
subject to the university's data-protection rules and are available from the
author on reasonable request. The 2020-II survey and interview data belong to
the master's thesis that designed the original intervention and are reported
there.

## Citing

Cite the article. To cite this package, use the DOI in the badge above; the
`CITATION.cff` file carries the same information in machine-readable form.
