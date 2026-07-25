# Methodology selection and research ethics

Read this when the student has not yet chosen a research design, or when drafting Chapter 3. Adapted from the research design patterns in Academic Research Skills (Cheng-I Wu, CC BY-NC 4.0), reduced to the designs viable inside a 15,000-word MBA dissertation and stripped of the systematic-review machinery that does not fit this scale.

## Part 1 — Choosing a design

The rubric rewards *justification against alternatives*, not description. Whichever design is chosen, Chapter 3 must show the alternatives were considered and explain why they lost.

### Viable designs at this scale

**Cross-sectional survey (quantitative)**
- Use when: testing hypothesised relationships between measurable constructs across a population
- Needs: validated scales, 150-300 usable responses, access to a defined sampling frame
- Analysis: descriptive statistics, reliability, regression or PLS-SEM
- Strength: tests theory, produces generalisable claims within the sampled population
- Weakness: cannot establish causation; common method bias if all constructs come from one self-report instrument
- Watch for: sample size feasibility. This is the most common point of collapse.

**Semi-structured interviews (qualitative)**
- Use when: the mechanism is not yet understood well enough to measure, or the RQ asks *how* or *why*
- Needs: 12-20 participants typically, until thematic saturation; interview protocol; recording and transcription
- Analysis: thematic analysis (Braun and Clarke's six phases is the standard reference), or template analysis
- Strength: surfaces mechanisms and unexpected explanations; strong fit for a practitioner-researcher with industry access
- Weakness: no generalisability claim; researcher bias in coding must be addressed explicitly
- Watch for: a practitioner interviewing their own colleagues creates a power-relation problem the ethics section must handle

**Single or comparative case study**
- Use when: the phenomenon cannot be separated from its context, or contrasting two settings is the point
- Needs: multiple data sources within each case - documents, interviews, observation, internal data
- Analysis: within-case analysis first, then cross-case pattern matching
- Strength: depth; strong for organisational research where the researcher has access
- Weakness: case selection must be justified theoretically, not by convenience
- Watch for: "I picked my employer because I work there" is not a case selection rationale. The theoretical reason must come first.

**Secondary data analysis**
- Use when: adequate published or institutional data exists - central bank statistics, World Bank indicators, regulatory filings, published survey microdata
- Needs: a dataset the student can legally access and that actually measures the constructs
- Analysis: whatever the data supports - panel regression, trend analysis, comparative statistics
- Strength: removes data collection risk entirely; large samples; strong feasibility
- Weakness: constructs are defined by whoever collected the data, not by the researcher; measurement may not match the theory
- Watch for: the gap between what the dataset measures and what the RQ asks. This must be discussed honestly, not hidden.

**Document or content analysis**
- Use when: the research object is text - policy documents, annual reports, regulatory guidance, disclosures
- Needs: a defined corpus with explicit inclusion criteria; a coding scheme
- Analysis: content analysis with coding frame, or thematic analysis of documents
- Strength: no participant recruitment, no ethics approval burden in most cases
- Weakness: documents record what organisations say, not what they do

**Mixed methods (sequential explanatory)**
- Use when: quantitative results need qualitative explanation, or a construct needs qualitative development before measurement
- Needs: both of the above, in sequence
- Strength: strong contribution claim
- Weakness: **usually too ambitious for 15,000 words and a single submission window.** Recommend only when both components are small and the timeline is genuinely comfortable.

### Selection questions

Work through these in order. The answers select the design.

1. Does the RQ ask *whether and how much* (→ quantitative) or *how and why* (→ qualitative)?
2. Are the constructs already well defined and measurable with validated scales, or still being explored?
3. What data can the student actually obtain, confirmed rather than assumed?
4. How many weeks remain before submission, and does the design fit inside that with collection, analysis and writing?
5. What does the literature in this specific area typically do, and is there a defensible reason to depart from it?

Question 3 outranks the others. An elegant design with no obtainable data is worse than a modest design that can be executed.

### Sample size reference

Quantitative, if a survey is chosen:

| Analysis | Minimum |
|---|---|
| Multiple regression | 50 + 8 × (number of predictors) |
| Exploratory factor analysis | 5-10 responses per measured item |
| PLS-SEM | 10 × the largest number of paths into any construct, as a floor; run a power analysis; in practice aim for 200+ |
| Covariance-based SEM | 200 minimum, 300+ for complex models |

Qualitative: justify by saturation rather than by number, but state the expected range and the stopping rule in advance.

## Part 2 — Research ethics

Section 3.10 is required. Beyond compliance, a thin ethics section is a visible signal to markers that the research design was not thought through.

### Human subjects decision tree

```
Does the research collect or analyse data from people?
│
├── No ─────────────────────────────► No human subjects review needed
│                                     (pure desk research, published statistics,
│                                      document analysis of organisational texts)
│
└── Yes
    │
    ├── Is the data already published and fully anonymous?
    │   └── Yes ──────────────────────► Usually exempt; confirm with the
    │                                    supervisor rather than assuming
    │
    ├── Is the data existing organisational data (not collected for this study)?
    │   ├── Already de-identified ────► Usually light-touch review;
    │   │                               organisational permission still required
    │   └── Contains identifiable data ► Full review; de-identification plan
    │                                    required before access
    │
    └── Direct interaction with participants (survey, interview, observation)?
        └── Yes ──────────────────────► Full ethics process:
                                         consent, information sheet,
                                         withdrawal rights, data handling plan
```

Staffordshire and BUV have their own ethics approval route and forms. Confirm the process and the lead time with the supervisor early - approval delays are a common cause of missed deadlines, and the process cannot be run retrospectively.

### The organisational data problem

This applies whenever a student proposes to use data from their own employer, and it applies with particular force in regulated sectors such as banking, healthcare and insurance.

Questions that must be answered **before the topic is locked**, not after:

- [ ] Has formal permission been requested, in writing, from someone with authority to grant it?
- [ ] What was the answer? An informal "should be fine" from a colleague is not permission.
- [ ] Is the data commercially sensitive or covered by banking secrecy, data protection law, or regulatory confidentiality obligations?
- [ ] Does it contain customer-level information? If so, can it be aggregated or de-identified before it leaves the organisation?
- [ ] Does the employment contract or an NDA restrict use of internal data for external publication?
- [ ] Will the dissertation need to be marked "PRIVATE & CONFIDENTIAL" to keep it out of the university library?
- [ ] If permission is withdrawn late, what is the fallback design?

The last question is the important one. A dissertation whose survival depends on continued organisational goodwill carries a risk that should be mitigated by design, not by hope. A fallback using public or aggregate data is worth planning even if it is never used.

### Practitioner-researcher positionality

When the researcher works inside the organisation being studied, three issues need explicit treatment in Chapter 3:

**Power relations.** Interviewing subordinates, or colleagues who know the researcher's role, affects what people say. Address it: how was voluntariness protected, were participants selected from outside the researcher's reporting line, how was confidentiality assured?

**Insider bias.** Domain familiarity is an asset for insight and a liability for interpretation, because the researcher already believes things about the answer. Name the prior beliefs and describe what was done to test them rather than confirm them.

**Dual role disclosure.** Participants must know they are speaking to a researcher, not to a colleague, and what will happen to what they say.

Handled well, positionality is a strength that appears in the individual-insight criterion. Left unaddressed, it is the first thing a methodologically alert marker will ask about.

### Ethics section checklist

- [ ] Informed consent process described, with the information provided to participants
- [ ] Voluntary participation and right to withdraw, including withdrawal after the fact
- [ ] Anonymity or confidentiality, and which one is being offered - they are different promises
- [ ] Data storage, security, retention period and disposal
- [ ] Approval status and reference, or a statement of why approval was not required
- [ ] Organisational permission where internal data is used
- [ ] Positionality where the researcher is an insider
- [ ] Any conflict of interest
