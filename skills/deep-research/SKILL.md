---
name: deep-research
description: Locate, verify, evaluate and synthesise academic sources for a Staffordshire MBA dissertation, organised by the geographic relevance cascade Vietnam first, then Southeast Asia, Asia, Europe/Americas, and global, with explicit transferability reasoning whenever non-Vietnamese evidence is used. Use this skill whenever the user needs to find literature, check whether a source is credible or even real, build a literature matrix, gather theory for a conceptual framework, find validated measurement instruments, or assemble research material against a chapter outline. Trigger on requests like "find papers on X", "what does the literature say about Y", "I need sources for section 2.3", or "is this citation real".
---

# Academic source research and synthesis

This skill produces verified research material organised against a chapter structure. It does not write dissertation prose. Its output is an input: a matrix of what the literature says, where the contradictions sit, and where the gap is.

## Rule one - nothing enters the record unverified

Language models generate citations that look completely plausible and do not exist. The author is real, the journal is real, the year is reasonable, and the paper was never written. A 2026 audit of 111 million references across 2.5 million papers estimated roughly 147,000 fabricated citations in 2025 alone. A marker checking one suspicious reference on Google Scholar takes thirty seconds, and under Staffordshire's academic misconduct policy a fabricated reference is not a slip.

So: **search the web for every source. Never produce a reference from memory.**

Each source carries one of three states:

| State | Meaning | Use |
|---|---|---|
| **VERIFIED** | Found in a bibliographic index or on the publisher site; metadata matches | Citable |
| **UNVERIFIABLE** | Plausible source not indexed internationally - common for Vietnamese journals, local reports, institutional publications | Citable only after the student obtains the document and confirms it |
| **NOT FOUND** | Searched thoroughly; no trace | Discard. Do not repair the metadata and re-offer it. |

Warning signs of fabrication: a title that fits the search terms unnaturally well; a real author who has never published in that area; a real journal where the volume, issue and year do not align; page numbers outside the issue's range; several sources sharing a suspiciously similar shape.

When a source cannot be verified, say so. Never invent a reference to fill a hole in an argument - flag the hole as `[SOURCE NEEDED]` instead.

## Rule two - the geographic cascade

Search in this order and stop expanding once sufficient evidence exists at a level:

```
1. Vietnam
2. Southeast Asia (Indonesia, Thailand, Philippines, Malaysia, Singapore)
3. Asia (with attention to comparable-income and comparable-institution markets)
4. Europe / Americas
5. Global / cross-country studies
```

**Whenever evidence comes from outside Vietnam, a transferability argument is mandatory.** Non-Vietnamese evidence is not automatically applicable, and asserting it is applicable without argument is exactly what markers penalise as uncritical use of sources. The argument must engage at least two of:

| Dimension | Questions to answer |
|---|---|
| Economic structure | Comparable income level, financial depth, banking penetration? |
| Institutional and regulatory | Similar supervisory regime, legal tradition, enforcement capacity? |
| Market maturity | Is the phenomenon at a comparable stage of development? |
| Cultural | Power distance, uncertainty avoidance, collectivism where behaviour is the outcome |
| Demographic | Age structure, urbanisation, digital adoption |

Write it in the form: *Evidence from [market] is used here because [dimension A] and [dimension B] are comparable to Vietnam; the principal limit on transferability is [dimension C], which suggests the effect size may [direction] in the Vietnamese case.*

That last clause matters. A transferability argument that finds no limits is not an argument, it is an assertion.

Where Vietnamese evidence is genuinely absent, say so explicitly and treat it as part of the gap - an under-studied context is a legitimate contribution claim under the Dissertation Guide's Strategy 3.

## Rule three - source credibility hierarchy

Work down this list. Upgrade weak sources before they reach the reference list.

1. Peer-reviewed journal articles (ABS 3* and above preferred)
2. Conference papers from top-tier venues
3. Academic books from major scholarly publishers
4. Institutional reports - World Bank, IMF, OECD, ADB, BIS, central banks
5. Government and regulatory publications - State Bank of Vietnam, GSO, ministry publications
6. Industry-grade sources - established market research, Statista, Bloomberg
7. Company reports and news - non-statistical claims only

Automatic replacements:

| Weak | Replace with |
|---|---|
| Wikipedia | The original academic source it cites |
| News article carrying a statistic | The central bank, statistical office or original study |
| Commercial market report | World Bank / ADB / OECD equivalent |
| Textbook citing a seminal study | The seminal study itself |
| Blog or vendor white paper | Peer-reviewed paper or institutional source |

The Dissertation Guide is explicit: use primary sources, avoid citing textbooks that cite the original study, and do not pad the reference list with sources that were not actually engaged with.

## Volume targets

For a 15,000-word Master's dissertation:

| Type | Minimum |
|---|---|
| Peer-reviewed articles | 30 |
| Institutional / regulatory sources | 8 |
| Industry-grade sources | 5 |
| **Total** | **50-70** |

Composition rule: the majority from the last ten years, plus a smaller set of foundational seminal works cited from the original. A reference list of only recent papers signals no theoretical grounding; a list of only old ones signals no engagement with the current field.

## Search strategy - record it before searching

```
Concept 1 terms: [primary] OR [synonym] OR [related construct]
Concept 2 terms: ...
Context terms: Vietnam OR "Viet Nam" OR "Southeast Asia" OR "emerging market"
Date range: [typically last 10 years for empirical, unrestricted for theory]
Inclusion criteria: [e.g. empirical studies reporting effect sizes]
Exclusion criteria: [e.g. non-peer-reviewed, predatory venues]
Databases: Google Scholar, Semantic Scholar, ScienceDirect, JSTOR, SSRN, VJOL
```

Recording this makes Chapter 3 defensible and lets the student answer "why is study X missing" without improvising.

## Literature matrix

The core deliverable. Build it as a table:

| Author (Year) | Market & sample | Theory used | IV / mediator / moderator / DV | Method | Key finding | Effect size | Author's stated limitation | Verified |
|---|---|---|---|---|---|---|---|---|

Two columns earn their keep disproportionately:

**Author's stated limitation.** What a previous author admits their study could not do is the most defensible gap available, and citing it demonstrates the paper was actually read rather than skimmed from the abstract.

**Effect size.** Collecting these makes it possible to say whether findings across studies actually agree, rather than just noting that both were significant.

Then read the matrix **down the columns, not across the rows**. Reading down "Key finding" exposes where the field agrees and where it contradicts itself. That pattern is the spine of the literature review, and it is what turns a list of summaries into an argument.

## Instrument and construct capture

For quantitative work, record for every construct:

- Original scale source, author and year
- Number of items
- Reported reliability in the original study
- Whether it has been validated in Vietnam or a comparable market
- Whether translation and back-translation would be required

If a scale has never been used in Vietnamese, flag that a pilot study and translation protocol will be needed - it belongs in Chapter 3 and markers ask about it.

## Contradiction inventory

Actively hunt for disagreement. A literature review in which every study agrees indicates insufficient reading, and contradictions are the richest source of a genuine research question.

```
Contradiction: [Study A] finds [X]; [Study B] finds [not X]
Possible explanations: [sample / market / measurement / time period / method]
Implication for this study: [what design decision this forces]
```

## Harvard capture format

Record complete metadata at the moment of finding, not later.

```
Journal article
Author, A.B. and Author, C.D. (Year) 'Article title.' Journal Name,
  Volume(Issue), pp. X-Y. doi:https://doi.org/...

Book
Author, A.B. (Year) Title of Book. Edition. Place: Publisher.

Chapter in edited book
Author, A.B. (Year) 'Chapter title.' In: Editor, C.D. (ed.) Book Title.
  Place: Publisher, pp. X-Y.

Report
Organisation (Year) Title of Report. Place: Publisher.

Website
Organisation (Year) Title of Page. Available at: URL (Accessed: Day Month Year).
```

In-text: `(Author, Year)`, `(Author et al., Year)` for three or more, `(Author A, Year; Author B, Year)` for multiple sources, and `(Author, Year: page)` when a page reference is needed. Alphabetical order in the list; only sources actually cited in the text appear there.

## Output format

Deliver research material mapped to the chapter outline, so it can be used section by section:

```
## Section 2.3 - [Section title from the approved outline]

**Argument this section must support**: [from the structure skill]

**Evidence available**
- [Author, Year] — [finding] — [market] — [VERIFIED]
- [Author, Year] — [finding] — [market] — [VERIFIED] — transferability: [argument]

**Contradiction present**: [if any]
**Gap**: [what is not covered]
**[SOURCE NEEDED]**: [claims the outline requires but no evidence was found for]
```

The `[SOURCE NEEDED]` markers are the useful part of the output. They tell the student exactly where the argument currently has no support, which is information they cannot get any other way.
