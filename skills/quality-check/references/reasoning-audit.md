# Reasoning audit reference

Diagnostic tools for challenging a draft. Adapted from the logical fallacy catalogue, argumentation framework and statistical reporting standards in Academic Research Skills (Cheng-I Wu, CC BY-NC 4.0), narrowed to what applies to a business dissertation.

---

## 1. Fallacies to hunt for

Most dissertation reasoning failures cluster in three families. Check these before anything else.

### Causal fallacies — the highest-frequency failure in quantitative business dissertations

| Fallacy | What it looks like | Test |
|---|---|---|
| **Cum hoc** (correlation ≠ causation) | Survey finds X correlates with Y; discussion says X improves Y | Is the data cross-sectional? Then no causal verb is available |
| **Post hoc** | Y changed after X was introduced, therefore X caused it | What else changed in the same period? |
| **Reverse causation** | X is claimed to drive Y when Y plausibly drives X | Could the arrow point the other way? Argue why not |
| **Ecological fallacy** | Country- or firm-level pattern used to make claims about individuals | At what level was the data measured, and at what level is the claim made? |
| **Simpson's paradox** | Aggregate relationship reverses within subgroups | Has the relationship been checked within relevant segments? |
| **Omitted variable** | A third factor drives both X and Y | Which plausible confound is not in the model, and why not? |

### Evidence fallacies

| Fallacy | What it looks like | Test |
|---|---|---|
| **Cherry-picking** | Only supporting studies cited; contradicting ones absent | Which studies disagree, and where are they in Chapter 2? |
| **Survivorship bias** | Only successful firms, adopters or customers sampled | Where are the failures, the non-adopters, the churned? |
| **Hasty generalisation** | Broad claims from a small or narrow sample | Who exactly does this finding apply to? |
| **Anecdotal evidence** | Professional experience presented as evidence rather than as illustration | Is this doing analytical work, or is it decoration? |
| **Appeal to authority** | A consultancy report or well-known name treated as settling a question | What is the underlying evidence, and is the source peer-reviewed? |

### Measurement and metric fallacies — particularly relevant to finance, credit and performance topics

| Fallacy | What it looks like | Test |
|---|---|---|
| **Goodhart's Law** | A metric used as a target has stopped measuring what it used to measure | Is this indicator being managed to, and does that corrupt it? |
| **McNamara fallacy** | What is easily quantified is treated as all that matters | What important effect is being excluded because it is hard to measure? |
| **Texas sharpshooter** | Patterns identified after seeing the data, presented as if hypothesised | Were the hypotheses fixed before the analysis was run? |
| **Base rate neglect** | Model accuracy claimed without reference to the underlying event rate | What is the base rate, and does the model beat it? |
| **Regression to the mean** | Improvement after intervention on an extreme group treated as an effect | Would this group have improved anyway? |

### Fast detection questions

| Ask | Detects |
|---|---|
| "Could B have other causes?" | Post hoc, omitted variable |
| "Where are the cases that failed?" | Survivorship bias |
| "Is this sample representative of the population you are claiming about?" | Hasty generalisation, ecological fallacy |
| "Were the criteria fixed before you saw the results?" | Texas sharpshooter, moving goalposts |
| "Is this term used the same way in Chapter 2 and Chapter 4?" | Equivocation |
| "What is the base rate?" | Base rate neglect |
| "Does the relationship hold within each segment?" | Simpson's paradox |

---

## 2. Toulmin audit of a central claim

Take the dissertation's main claim and identify all six components. A missing component is a specific, fixable weakness.

| Component | Question | Red flag |
|---|---|---|
| **Claim** | What is being asserted? | Thesis shifts between chapters |
| **Data** | What evidence supports it? | Assertion without empirical backing |
| **Warrant** | *Why* does that evidence support that claim? | Logical gap between data and conclusion |
| **Backing** | What justifies the warrant itself? | Methodological validity assumed |
| **Qualifier** | How certain is the claim? | Absolute language |
| **Rebuttal** | What would undermine it? | No limitations acknowledged |

The warrant is the component most often missing and least often noticed. Evidence presented without a warrant is information, not argument — which is exactly the "describes rather than argues" failure the rubric penalises.

---

## 3. Causal claim test

When a dissertation claims X causes Y, check how many of these hold. Temporality is mandatory; the rest are cumulative.

1. **Strength** — is the association large enough to matter?
2. **Consistency** — replicated across studies or contexts?
3. **Specificity** — does X lead to Y in particular, or to everything?
4. **Temporality** — does X demonstrably precede Y? *(required)*
5. **Gradient** — does more X produce more Y?
6. **Plausibility** — is there a stated mechanism?
7. **Coherence** — consistent with what else is known?
8. **Experimental evidence** — any, anywhere?
9. **Analogy** — do similar causes produce similar effects elsewhere?

Fewer than three satisfied means the causal claim is unsupported and the language must be downgraded to association.

---

## 4. Alternative explanations

For every substantive finding, at least two competing explanations should have been considered and addressed. A discussion that entertains only the author's preferred interpretation is confirmation bias regardless of how well written it is.

Evaluate each candidate explanation on:

- **Scope** — how much of the observed pattern does it account for?
- **Simplicity** — how many additional assumptions does it need?
- **Fit** — is it consistent with other known findings?
- **Predictive power** — does it imply anything testable?

The strongest explanation is the one that wins across all four, not the one that matches the hypothesis.

---

## 5. Epistemic status of claims

Match language to evidence. Overclaiming is among the most common quality problems at Master's level and is easy for a marker to spot.

| Status | Meaning | Language available |
|---|---|---|
| **Established** | Replicated, high consensus | "X is..." |
| **Supported** | Evidence exists, not yet replicated | "Evidence indicates that X..." |
| **Preliminary** | Single study, small sample | "Preliminary findings suggest..." |
| **Speculative** | Reasoned, not directly evidenced | "It may be that...", "a plausible reading is..." |
| **Contested** | Conflicting evidence | "While some studies find X, others report..." |

Findings from the student's own single-study dissertation are almost never above *Preliminary* or *Supported*. Language in Chapter 4 and Chapter 5 should reflect that.

---

## 6. Own-data integrity checks

These apply to the student's own analysis, not to their sources. The concern is that plausible-looking numbers can be produced by a broken process, and a wrong number reads exactly like a right one.

| Check | Question | Signal of a problem |
|---|---|---|
| Provenance | Can every number in the draft be traced to a saved output file? | Numbers that exist only in the draft |
| Reproducibility | Would re-running the analysis produce the same figures? | No saved syntax, no saved dataset version |
| Suspicious roundness | Are any effect sizes exactly 0.5, exactly double, exactly zero variance? | Round values often mean a constant leaking through a broken step |
| Variation | Do confidence intervals and standard errors actually differ across conditions? | Identical error terms across different groups |
| Sample arithmetic | Do the group sizes sum to the reported total? | Silent case deletion |
| Attrition | Is every dropped case accounted for? | Unexplained gap between collected and analysed |
| Table-to-text match | Does each number in the prose match the table it refers to? | Transcription drift between drafts |

Ask directly: *show me the file this number came from.* If it cannot be produced, that is the finding.

---

## 7. Statistical reporting standards

Style-neutral; applies regardless of referencing system.

**Descriptive statistics** — report mean with standard deviation (not standard error), both total and group sample sizes, range or interquartile range, and raw frequencies alongside percentages for categorical variables.

**Effect sizes are obligatory, not optional.** Reporting significance without magnitude is a substantive omission, because with a large sample a trivially small effect will be significant.

| Test | Effect size | Small / Medium / Large |
|---|---|---|
| t-test | Cohen's d | 0.2 / 0.5 / 0.8 |
| ANOVA | eta squared | .01 / .06 / .14 |
| Correlation | r | .10 / .30 / .50 |
| Regression | f squared | .02 / .15 / .35 |
| Chi-square | Cramér's V | .10 / .30 / .50 |
| Logistic regression | Odds ratio | 1.5 / 2.5 / 4.3 |

Report the number *and* interpret its magnitude in business terms. An effect that is statistically significant but managerially trivial should be described as such — saying so demonstrates judgement rather than weakness.

**Confidence intervals** — report 95% CI for key estimates in the form `95% CI [lower, upper]`, and interpret the width, not merely whether it excludes zero.

**Significance** — report exact p values (`p = .032`). Never write `p = .000`; use `p < .001`. State the alpha level in advance. Apply a correction when running multiple comparisons. Report non-significant results fully — selectively reporting only significant findings is a form of data misrepresentation.

**Reliability and validity** — for scale-based work, report Cronbach's alpha (≥ .70), and for factor work report KMO, Bartlett's test, factor loadings (≥ .50), variance explained (≥ 50%), composite reliability (≥ .70) and AVE (≥ .50). For SEM, report model fit indices with their thresholds and their sources.

**Common method bias** — where all constructs are measured by a single self-report instrument at one time point, this must be tested and reported. Harman's single-factor test is the minimum; a marker will ask.

---

## 8. Self-plagiarism

Staffordshire lists self-plagiarism explicitly as academic misconduct. It applies to the student's own earlier coursework on the same programme.

- Reusing passages from a previous assignment without declaration is misconduct even though the words are the student's own
- Reusing the same literature is fine; reusing the same sentences is not
- If the dissertation builds on an earlier assignment, disclose it and cite it
- Check any module where the topic overlapped with the dissertation area

---

## Provenance note

The reasoning frameworks above are standard scholarly tools — Toulmin, Bradford Hill, Swales, inference to best explanation, Cohen's conventions — and can be cited from their original sources.

The ARS repository additionally cites several very recent papers for its AI-failure taxonomy that could not be verified here and postdate available knowledge. Use the *checks* in section 6, which stand on their own reasoning, but do not cite those specific papers in the dissertation without independently verifying that they exist and say what they are claimed to say.
