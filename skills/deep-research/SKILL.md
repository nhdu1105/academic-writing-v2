---
name: deep-research
description: Find, verify and evaluate academic and other credible sources for a Staffordshire MBA dissertation - for the literature review or for any other chapter the user names - and deliver them as a Literature Review Matrix spreadsheet in the user's fixed 12-column format. Searching is organised by the geographic relevance cascade Vietnam first, then Southeast Asia, Asia, Europe/Americas, and global, with explicit transferability reasoning whenever non-Vietnamese evidence is used. Use this skill whenever the user needs to find literature, check whether a source is credible or even real, build or extend a literature matrix, gather theory for a conceptual framework, find validated measurement instruments, or assemble research material against a chapter outline. Trigger on requests like "find papers on X", "what does the literature say about Y", "I need sources for section 2.3", "build me a literature matrix", or "is this citation real". Always confirm the topic, aims and objectives before searching if the request does not already state them.
---

# Academic source research and synthesis

This skill finds and verifies sources for a dissertation and hands them back as a structured
matrix. It does not write dissertation prose. Its output is an input to writing: what the
literature says, where the contradictions sit, and where the gap is.

Sources are for whichever part of the dissertation the user names. The literature review is the
default consumer, but the same search discipline serves the methodology chapter (validated
instruments, method precedents), the introduction (context statistics), and the discussion
(studies to agree or disagree with). Ask which, rather than assuming Chapter 2.

## Step 0 - clarify before searching

**Do not start searching on a thin prompt.** A search launched against a guessed topic burns
the user's time and returns a matrix they cannot use. Check whether the request already carries
the four essentials:

1. **Topic** - the phenomenon, the context, and the population or sector
2. **Aim / research question** - what the dissertation is trying to establish
3. **Objectives or constructs** - the specific variables, themes or sub-questions to find evidence for
4. **Where the sources are going** - which chapter or section, and roughly how many sources

If all four are present, or can be read off an outline, matrix or proposal the user has already
supplied in this conversation or in an uploaded file, **start searching**. Say what has been
assumed in one line and proceed; do not interrogate a user who has already done the work.

If something essential is missing, ask before searching. Ask the smallest number of questions
that unblock the search - one to three, never a long form. Use the interactive option tool when
available, since it is faster to tap than to type. Typical gaps and the question that closes them:

| Missing | Ask |
|---|---|
| Topic too broad ("fintech in Vietnam") | Which specific outcome or behaviour is being explained? |
| No research question | What is the aim - measure a relationship, explore a process, evaluate a case? |
| No constructs | Which variables or themes should the evidence cover? |
| No destination | Which chapter or section are these for? |
| No scope | Roughly how many sources, and any date or method restrictions? |
| Method unclear | Quantitative, qualitative, or mixed - this decides whether to capture scales |

One thing worth flagging early rather than at the end: if the topic as stated has almost no
Vietnamese empirical base, say so at clarification time and agree the cascade level before
searching, instead of returning a matrix of foreign studies the user was not expecting.

## Rule one - nothing enters the record unverified

Language models generate citations that look completely plausible and do not exist. The author
is real, the journal is real, the year is reasonable, and the paper was never written. A 2026
audit of 111 million references across 2.5 million papers estimated roughly 147,000 fabricated
citations in 2025 alone. A marker checking one suspicious reference on Google Scholar takes
thirty seconds, and under Staffordshire's academic misconduct policy a fabricated reference is
not a slip.

So: **search the web for every source. Never produce a reference from memory.**

Each source carries one of three states, recorded in the matrix's `Other notes` column:

| State | Meaning | Use |
|---|---|---|
| **VERIFIED** | Found in a bibliographic index or on the publisher site; metadata matches | Citable |
| **UNVERIFIABLE** | Plausible source not indexed internationally - common for Vietnamese journals, local reports, institutional publications | Citable only after the student obtains the document and confirms it |
| **NOT FOUND** | Searched thoroughly; no trace | Discard. Do not repair the metadata and re-offer it. |

Warning signs of fabrication: a title that fits the search terms unnaturally well; a real author
who has never published in that area; a real journal where the volume, issue and year do not
align; page numbers outside the issue's range; several sources sharing a suspiciously similar
shape.

When a source cannot be verified, say so. Never invent a reference to fill a hole in an argument
- flag the hole as `[SOURCE NEEDED]` instead.

## Rule two - the geographic cascade

Search in this order and stop expanding once sufficient evidence exists at a level:

```
1. Vietnam
2. Southeast Asia (Indonesia, Thailand, Philippines, Malaysia, Singapore)
3. Asia (with attention to comparable-income and comparable-institution markets)
4. Europe / Americas
5. Global / cross-country studies
```

**Whenever evidence comes from outside Vietnam, a transferability argument is mandatory.**
Non-Vietnamese evidence is not automatically applicable, and asserting it is applicable without
argument is exactly what markers penalise as uncritical use of sources. The argument must engage
at least two of:

| Dimension | Questions to answer |
|---|---|
| Economic structure | Comparable income level, financial depth, banking penetration? |
| Institutional and regulatory | Similar supervisory regime, legal tradition, enforcement capacity? |
| Market maturity | Is the phenomenon at a comparable stage of development? |
| Cultural | Power distance, uncertainty avoidance, collectivism where behaviour is the outcome |
| Demographic | Age structure, urbanisation, digital adoption |

Write it in the form: *Evidence from [market] is used here because [dimension A] and
[dimension B] are comparable to Vietnam; the principal limit on transferability is
[dimension C], which suggests the effect size may [direction] in the Vietnamese case.*

That last clause matters. A transferability argument that finds no limits is not an argument, it
is an assertion. The argument goes in the `Other notes` column of the matrix for every
non-Vietnamese row.

Where Vietnamese evidence is genuinely absent, say so explicitly and treat it as part of the gap
- an under-studied context is a legitimate contribution claim under the Dissertation Guide's
Strategy 3.

## Rule three - source credibility hierarchy

Work down this list. Upgrade weak sources before they reach the matrix.

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

The Dissertation Guide is explicit: use primary sources, avoid citing textbooks that cite the
original study, and do not pad the reference list with sources that were not actually engaged
with.

## Volume targets

For a 15,000-word Master's dissertation, across the whole project:

| Type | Minimum |
|---|---|
| Peer-reviewed articles | 30 |
| Institutional / regulatory sources | 8 |
| Industry-grade sources | 5 |
| **Total** | **50-70** |

A single request will usually cover one section, so scale to what was asked and track the
running total against these figures rather than dumping seventy rows at once.

Composition rule: the majority from the last ten years, plus a smaller set of foundational
seminal works cited from the original. A reference list of only recent papers signals no
theoretical grounding; a list of only old ones signals no engagement with the current field.

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

Recording this makes Chapter 3 defensible and lets the student answer "why is study X missing"
without improvising. Hand it back alongside the matrix.

## The deliverable - Literature Review Matrix

**The primary output is a spreadsheet in the user's fixed format.** Twelve columns, in this
order, with the header wording taken verbatim from
`assets/literature_matrix_template.xlsx`. Do not add, remove, rename or reorder columns.

| # | Column | What goes in it |
|---|---|---|
| A | Author | Harvard form: `Surname, A.B. and Surname, C.D.`; `et al.` for four or more |
| B | Year Publication | Publication year only |
| C | Journal Name | Journal, or publisher / issuing body for books and reports |
| D | Title of paper | Full title, sentence case |
| E | Citation Count | Google Scholar count with the date checked; `n/a` for reports |
| F | Theory / Framework used | Named theory and its originator, e.g. `UTAUT2 (Venkatesh et al., 2012)`; `none stated` is a finding worth recording |
| G | Methods | Design, sample size, population and **market**, analysis technique |
| H | Results / Findings | The specific result, **with effect sizes and significance** where reported - not "found a positive relationship" |
| I | Controveries / Diagreements with other authors | Which study in the matrix this one contradicts, and on what |
| J | Limitations | **The authors' own stated limitations**, in their terms |
| K | Implications for theory / practice | What the authors claim follows |
| L | Other notes | Verification state, DOI or URL, transferability argument for non-Vietnamese evidence, scale details, and the section this feeds |

Three of these carry more weight than their size suggests:

**Column J, the authors' stated limitations.** What a previous author admits their study could
not do is the most defensible gap available, and citing it demonstrates the paper was actually
read rather than skimmed from the abstract.

**Column H, effect sizes.** Collecting these makes it possible to say whether findings across
studies actually agree, rather than just noting that both were significant.

**Column I, disagreements.** Fill it by comparing each new row against rows already in the
matrix. A matrix with column I entirely blank means the reading was too narrow, not that the
field is settled.

Then read the matrix **down the columns, not across the rows**. Reading down `Results /
Findings` exposes where the field agrees and where it contradicts itself. That pattern is the
spine of the literature review, and it is what turns a list of summaries into an argument. State
the two or three patterns found, in the chat reply, when handing over the file.

### Building the file

Collect the verified sources as JSON - a list of objects taking the keys `author, year, journal,
paper_title, citations, theory, methods, findings, controversies, limitations, implications,
notes`, mapped to columns A-L in order. Then write the script at the end of this file to
`build_matrix.py` and run it:

```bash
python build_matrix.py sources.json /mnt/user-data/outputs/Literature_Review_Matrix.xlsx \
  --title "Literature Review Matrix - <topic>"
```

Rows are sorted alphabetically by author. Present the result with `present_files` - a file
written but not presented cannot be opened.

Two format notes. The column I and K headers contain spelling slips (`Controveries /
Diagreements`, and a trailing space in `Implications for theory / practice `); these reproduce
the user's own template verbatim so their files stay consistent, and correcting them is offered
rather than done unasked. And when the user is extending a matrix they already have, edit
**their** file - load it, append below the last row, and match its existing conventions - rather
than generating a fresh one.

If the user explicitly asks for the matrix in chat instead of as a file, render the same twelve
columns as a markdown table and skip the script.

## Section-mapped companion notes

Alongside the spreadsheet, hand back a short section-by-section note, so the matrix can be used
while writing:

```
## Section 2.3 - [Section title from the approved outline]

**Argument this section must support**: [from the structure skill]
**Rows supporting it**: [Author, Year] · [Author, Year] · [Author, Year]
**Contradiction present**: [if any]
**Gap**: [what is not covered]
**[SOURCE NEEDED]**: [claims the outline requires but no evidence was found for]
```

The `[SOURCE NEEDED]` markers are the useful part of this output. They tell the student exactly
where the argument currently has no support, which is information they cannot get any other way.

## Instrument and construct capture

For quantitative work, record in column L for every construct:

- Original scale source, author and year
- Number of items
- Reported reliability in the original study
- Whether it has been validated in Vietnam or a comparable market
- Whether translation and back-translation would be required

If a scale has never been used in Vietnamese, flag that a pilot study and translation protocol
will be needed - it belongs in Chapter 3 and markers ask about it.

## Contradiction inventory

Actively hunt for disagreement. A literature review in which every study agrees indicates
insufficient reading, and contradictions are the richest source of a genuine research question.
Column I holds the short version; expand the significant ones in the companion notes:

```
Contradiction: [Study A] finds [X]; [Study B] finds [not X]
Possible explanations: [sample / market / measurement / time period / method]
Implication for this study: [what design decision this forces]
```

## Harvard capture format

Record complete metadata at the moment of finding, not later. The matrix columns hold enough to
rebuild any of these forms.

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

In-text: `(Author, Year)`, `(Author et al., Year)` for three or more, `(Author A, Year; Author B,
Year)` for multiple sources, and `(Author, Year: page)` when a page reference is needed.
Alphabetical order in the list; only sources actually cited in the text appear there.

---

## Appendix - build_matrix.py

Write this to `build_matrix.py` before running the command in *Building the file*. It needs
`openpyxl` only, and creates the matrix from scratch - no template file required.

```python
#!/usr/bin/env python3
"""Build a Literature Review Matrix spreadsheet from a JSON file of verified sources.

Usage:
    python build_matrix.py sources.json output.xlsx [--title "Literature Review Matrix - <topic>"]

Creates the fixed 12-column matrix. Column order and header wording are the
user's spec and must not be changed.
"""

import json
import sys
from pathlib import Path

import openpyxl
from openpyxl.styles import Alignment, Border, Font, Side

HEADERS = [
    "Author", "Year Publication", "Journal Name", "Title of paper",
    "Citation Count", "Theory / Framework used", "Methods",
    "Results / Findings", "Controveries / Diagreements with other authors",
    "Limitations", "Implications for theory / practice ", "Other notes",
]

FIELDS = [
    "author", "year", "journal", "paper_title", "citations", "theory",
    "methods", "findings", "controversies", "limitations", "implications", "notes",
]

WIDTHS = {"A": 22, "B": 12, "C": 24, "D": 34, "E": 12, "F": 22,
          "G": 30, "H": 38, "I": 30, "J": 28, "K": 30, "L": 34}

FONT = "Aptos Narrow"
THIN = Side(style="thin")
BORDER = Border(left=THIN, right=THIN, top=THIN, bottom=THIN)


def main() -> None:
    if len(sys.argv) < 3:
        sys.exit(__doc__)

    rows = json.loads(Path(sys.argv[1]).read_text(encoding="utf-8"))
    if not isinstance(rows, list):
        sys.exit("sources.json must contain a list of objects")
    rows.sort(key=lambda r: str(r.get("author", "")).lower())

    title = "Literature Review Matrix"
    if "--title" in sys.argv:
        title = sys.argv[sys.argv.index("--title") + 1]

    wb = openpyxl.Workbook()
    ws = wb.active

    ws.merge_cells("A2:K2")
    t = ws.cell(row=2, column=1, value=title)
    t.font = Font(name=FONT, size=16)
    t.alignment = Alignment(horizontal="center", vertical="center")
    ws.row_dimensions[2].height = 21

    for c, head in enumerate(HEADERS, start=1):
        cell = ws.cell(row=3, column=c, value=head)
        cell.font = Font(name=FONT, size=12)
        cell.border = BORDER
        cell.alignment = Alignment(horizontal="center", vertical="center", wrap_text=True)
    ws.row_dimensions[3].height = 60

    for i, row in enumerate(rows):
        for c, key in enumerate(FIELDS, start=1):
            cell = ws.cell(row=4 + i, column=c, value=row.get(key, ""))
            cell.font = Font(name=FONT, size=11)
            cell.border = BORDER
            cell.alignment = Alignment(wrap_text=True, vertical="top",
                                       horizontal="center" if c in (2, 5) else "left")

    for col, width in WIDTHS.items():
        ws.column_dimensions[col].width = width
    ws.freeze_panes = "A4"

    out = Path(sys.argv[2])
    out.parent.mkdir(parents=True, exist_ok=True)
    wb.save(out)
    print(f"Wrote {len(rows)} sources to {out}")


if __name__ == "__main__":
    main()
```
