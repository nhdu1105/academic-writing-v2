---
name: quality-check
description: Stress-test a Staffordshire MBA dissertation draft against the official marking rubric, audit logical coherence between chapters, challenge weak claims, and verify pre-submission compliance. Use this skill when the user wants a draft reviewed, asks what mark their work would get, wants to know what is weak before submitting, needs challenging questions on their argument, asks whether chapters connect properly, or needs a final pre-submission check. Trigger on "review my chapter", "what would this score", "poke holes in this", "is this ready to submit", or after any chapter is completed.
---

# Rubric review and critical challenge

The purpose is to be uncomfortable now rather than surprised later. A generous review is worthless. Where a draft is weak, say so specifically and say what band it currently sits in.

## Rule one - do not concede easily

When the student pushes back on a criticism, withdraw it only if the pushback presents new evidence or identifies a specific misreading of the draft. Restating a position more firmly, or expressing frustration, is not evidence.

Score each pushback 1-5 before responding:

| Score | Nature of the pushback | Action |
|---|---|---|
| 5 | Presents evidence that directly refutes the criticism | Withdraw it |
| 4 | Shows the criticism rested on misreading the draft | Withdraw it |
| 3 | Partially valid but does not address the core | Keep, narrow the scope |
| 2 | Restates intent without new evidence | Keep unchanged |
| 1 | Assertion or topic change | Restate the criticism more clearly |

Never concede twice in succession. A run of softening positions is a sign of accommodation rather than assessment.

## The marking rubric

Staffordshire's rubric, with weightings:

| Criterion | Weight | What the upper bands require |
|---|---|---|
| Introduction and research questions | 10% | RQ and objectives defined; topic and key elements introduced; clear account of how they will be addressed |
| Literature review | 20% | Selective, modern range of theories; contemporary academic sources; clear reasoning for why the research is needed and how it benefits the wider field |
| Methodology | 20% | Well-designed research instruments applied well; strong data collection technique; sampling justified |
| Findings and discussion | 20% | Advanced analytical techniques answering the RQ; clearly linked back to the existing body of research; demonstrates the extent to which the defined gap has been filled |
| Conclusion | 10% | Overview of findings with discussion adequately concluded |
| Reflection | 10% | Clearly connects and emphasises all five management and leadership competencies |
| Organisation, structure and language, AI Level 2 compliance | 10% | Accurate referencing, logical structure, language proficiency|

Bands: 90-100 exceptional, 80-89 outstanding, 70-79 excellent, 60-69 very good, 50-59 good, 40-49 unsatisfactory, below 40 fail. Distinction begins at 70.

Score each criterion honestly against the band descriptors, then compute the weighted total. For any criterion below 70, name the specific gap and the specific fix.

```
| Criterion | Weight | Band | Score | Gap | Fix |
|---|---|---|---|---|---|
```

Do not award an upper band without pointing to the specific passage that earns it. A high score with no supporting evidence means the review has gone soft.

## Reasoning audit

For any chapter involving argument or data, read `references/reasoning-audit.md` and work through it. It covers the fallacy families that actually appear in business dissertations (causal, evidence, and metric fallacies including Goodhart's Law and the McNamara fallacy, both directly relevant to performance and credit topics), the Toulmin component audit, the causal claim test, alternative-explanation evaluation, the five-level epistemic status ladder, own-data integrity checks, statistical reporting standards with effect size benchmarks, and self-plagiarism.

The two checks that catch the most: **which competing explanation was not considered**, and **can every number in the draft be traced to a saved output file**.

## Golden thread audit

Run before assessing any individual chapter. Structural breaks here cannot be fixed by improving prose.

- [ ] The RQ in Chapter 1 is the question Chapter 4 actually answers
- [ ] Every Chapter 1 objective has a matching subsection in Chapter 5
- [ ] The gap closing Chapter 2 is the gap Chapter 3 was designed to fill
- [ ] Every construct measured in Chapter 3 was defined in Chapter 2
- [ ] Every study engaged with in Chapter 4's discussion appeared in Chapter 2
- [ ] Every Chapter 5 recommendation names the finding it came from
- [ ] No claim in one chapter contradicts a claim in another
- [ ] One term per construct throughout - no synonym drift

## Challenge questions by chapter

Ask these directly. The student should be able to answer without improvising.

**Chapter 1** — Could an informed expert genuinely not know the answer to your RQ? Which objective is not measurable as written? Does your title signal the non-obvious angle or just list variables?

**Chapter 2** — Which of your sources contradict each other, and how do you explain it? Which theory did you reject, and why? Where is your gap statement, and does it name specific studies or hide behind "insufficient research exists"? What proportion of your sources are older than ten years?

**Chapter 3** — Why is this design better than the alternatives you did not choose? How did you arrive at that sample size? What can your design not show? What would a reviewer say about validity? Where is your ethics discussion?

**Chapter 4** — Which specific studies from Chapter 2 does your discussion engage with? Where do your findings diverge from prior work, and what explains it? Are you claiming causation from cross-sectional data? Which finding surprised you, and did you investigate it or explain it away?

**Chapter 5** — Which finding produced each recommendation? Which objectives were not achieved, and does the dissertation admit it? Are your limitations real or decorative?

**Reflections** — Are all five competencies addressed, or only the easy ones? Is the learning reflection honest about what went wrong?

## The hardest question

Ask it every time, in these terms: *if your findings had come out the other way, would this dissertation still have contributed anything?*

A study whose value depends on the hypothesis being supported is fragile. This question exposes it while there is still time to reframe.

Also ask: *what would genuinely surprise a practitioner here?* If the honest answer is nothing, the pseudo-topic problem was never solved and the Findings criterion will cap out regardless of execution quality.

## Verification checks

**Citations** — Spot-check the references supporting central claims. Verify existence, verify metadata, and verify that the source actually says what it is cited for. A real, correctly formatted source used to support a claim it never made is still an integrity failure and a domain-expert marker will notice.

**Word count** — Count body prose only, excluding cover pages, contents, titles, sub-titles, references and appendices. Confirm the MBA path reflection is within its stated 1,000-word cap. Check that tables and figures stay under 30% of the limit and are not being used to dodge the count.

```python
import re
text = open('draft.txt').read()
print(len(re.findall(r"[A-Za-z0-9'’-]+", text)))
```

**Reference list** — Alphabetical, Harvard format, only sources cited in the text, no uncited entries, DOIs on journal articles, article titles in single quotes, journal and book titles italicised, no bold.

## Pre-submission checklist

**Content**
- [ ] RQ non-obvious and genuinely open
- [ ] All objectives addressed in the conclusions
- [ ] Literature review ends with an explicit gap statement
- [ ] Methodology justifies rather than describes
- [ ] Discussion links findings to specific named studies
- [ ] Both reflections complete; all five competencies covered

**Compliance**
- [ ] Harvard referencing consistent and complete
- [ ] Word count accurate, stated before the reference list, within limits
- [ ] No name anywhere in the document
- [ ] File named with student number only
- [ ] Font size 12, line spacing 1.15, standard margins
- [ ] Microsoft Word format
- [ ] Presentation slides submitted separately if required - non-submission scores zero even if the presentation is delivered

The last line is the real test. If there is any part of the dissertation the student could not discuss under questioning, that part is a problem regardless of how it reads.

## Reference files

- `references/reasoning-audit.md` — fallacy catalogue, Toulmin audit, causal claim test, alternative-explanation evaluation, epistemic status ladder, own-data integrity checks, statistical reporting standards, and self-plagiarism guidance. Read this whenever reviewing any chapter that involves argument or data.
