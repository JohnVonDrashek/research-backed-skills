# Contributing

Each skill lives in `skills/<name>/` with a `SKILL.md` and a `references/sources.md`.

## Evidence standard

1. Tag each rule in `SKILL.md` with one evidence tag: `exp`, `corr`, `count`, or `judgment`. Add `preprint` next to the main tag when the study lacks peer review.
2. Read the whole paper. Authors often write abstracts that claim more than their results sections show.
3. Add an entry to `references/sources.md` with:
   - the full citation and a DOI or arXiv link
   - the sample and what the study measured
   - each number the skill uses, with its table or section
   - the limits the authors state
4. Check the DOI against Crossref:

   ```bash
   curl -s https://api.crossref.org/works/10.1016/j.jss.2023.111806 | python3 -m json.tool | head -40
   ```

   Swap in your DOI and compare the title, authors, venue, and year.
5. Give the effect size beside any claimed effect, such as d = 0.31 for the installation finding in Liu 2022.
6. Describe `corr` and `count` findings as associations. Save causal verbs such as "increases" for `exp` findings.

## Judgment rules

Label judgment rules and give the reason in the same line, so readers can weigh it and disagree.

## Pull requests

Name the rule you added or changed and link the source entry. If a study contradicts an existing rule, open an issue with the citation.
