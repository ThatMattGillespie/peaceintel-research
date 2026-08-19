# Peace Intel — Research

Audience landing pages for the user-research sprint. Static design prototype for internal
review, not for distribution. No build step; every page is a single self-contained HTML file.

## Pages

| | |
|---|---|
| [Landing](https://thatmattgillespie.github.io/peaceintel-research/) | General landing page, with an audience routing strip at `#who` |
| [Audiences](https://thatmattgillespie.github.io/peaceintel-research/audiences.html) | Opens on a chooser, then reveals one of five audience versions |
| [Problem statements](https://thatmattgillespie.github.io/peaceintel-research/problems.html) | All five problem statements on one sheet, for interviews |

## How the audience page works

It opens on a fill-in-the-blank sentence — *"I work at ⌄a funding organization as a ⌄senior
leader."* — and reveals the matching version once both blanks are filled. Five combinations,
because practitioners exist on the implementer side only:

| | Senior Leadership | Program Managers | Practitioners |
|---|---|---|---|
| **Funding organization** | ✓ | ✓ | — |
| **Implementing organization** | ✓ | ✓ | ✓ |

Every state is a shareable URL, and **any link carrying both parameters skips the chooser**:

```
audiences.html?v=funders&role=senior-leadership
audiences.html?v=implementers&role=practitioners
```

`?v=` on its own opens the chooser with the organisation already filled in. `funders.html`,
`program-managers.html` and `practitioners.html` redirect to their equivalent state. Note that
`program-managers.html` was written for the funder side, so it lands on Funders → Program
Managers.

Hero, subhead, problem statement and closing CTA change per state; the use-case cards change
per side. Everything else is shared.

## Notes for reviewers

- Type is DIN 2014 (self-hosted from `Fonts/`), Nanum Myeongjo, and Space Mono.
- The use-case card graphics are static stills built in HTML/CSS from the real app components.
  They are not screenshots and not interactive.
- The problem cards are drawn from the Jobs-to-be-Done audit and selected by opportunity score
  (importance minus satisfaction). Two of the five audiences — implementer leadership and
  implementer program managers — have no rows in that audit yet, so those cards are written
  from the nearest jobs. `problems.html` labels which sets rest on the audit and which do not.

## Relationship to peaceintel-style-review

`peaceintel-style-review` is the earlier review site and remains live and untouched. It holds
its own copy of these pages plus `toggle-lab.html`, a record of the audience-toggle
alternatives explored before the chooser replaced them. **This repo is the current one for the
research sprint**; edits should land here.

## Open

- **Corpus stats.** The landing page still shows an older set of numbers than the audience page.
  The July 31 library metrics match the audience page; the landing page needs updating, pending
  a decision on whether to lead with one number instead of five.
- **Copy.** The AI-specific language ("corpus", "LLM agent", "machine-readable") is inventoried
  and awaiting a rewrite.
