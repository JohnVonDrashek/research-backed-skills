---
name: readme
description: Write, revise, or trim a project README using findings from published studies of GitHub READMEs. Use when creating a README, reviewing or shortening one, or choosing which sections it needs.
---

# README

Write READMEs from what four studies of GitHub projects found, and tell the user how strong each finding is. Each rule below carries one tag:

| Tag | Meaning |
|-----|---------|
| `corr` | A peer-reviewed study linked this to more GitHub stars. Popular projects may write fuller READMEs because they have more people, so the README may follow popularity instead of driving it. |
| `count` | A study counted what READMEs contain. It measured no outcome. |
| `preprint` | The study behind it has no peer review. |
| `judgment` | No study backs it. The rule states its reason. |

Keys such as [Liu 2022] point to [references/sources.md](references/sources.md), which gives each study's sample, method, numbers, and limits. Read it when the user asks why, or before you call a rule proven.

## Sections

Include a section when the project has material for it. Draft it from the code, manifest, and existing docs. Leave it out when you would have to guess what goes in it.

| Section | Tag | Evidence |
|---------|-----|----------|
| What the project does, at the top | `count` | 97% of 393 sampled READMEs had it [Prana 2019]. A description section showed a negligible link to stars (d = 0.04) [Liu 2022]. Readers expect it; it won't set a project apart. |
| Installation | `corr` | Small positive effect on stars (d = 0.31). 21% of 11,594 Java READMEs had one [Liu 2022]. |
| Usage with code examples | `corr` | Usage sections had a small effect (d = 0.31), and code snippets went with more stars [Liu 2022]. Popular repos averaged 6.2 code blocks; zero-star repos averaged 2.3 [Wang 2023]. |
| License | `corr` | d = 0.42, tied for the largest section effect [Liu 2022]. |
| Contributing | `corr` | d = 0.42 [Liu 2022]. Popular projects included contribution guidelines more often [Venigalla 2022, `preprint`]. |
| Links to docs, papers, related projects | `corr` | Link count had a large effect (Cliff's δ = 0.67) and stayed significant after controls for repository traits [Wang 2023]. |
| Why the project exists | `count` | 25.7% of READMEs had it, the rarest GitHub-recommended content [Prana 2019]. The authors argue a stated purpose sets a project apart from similar ones; they did not test that. |
| Table of contents, for long READMEs | `corr` | Small effect (d = 0.22). 2% of READMEs had one [Liu 2022]. |

## Format

- Put steps, options, features, and requirements in lists. `corr`: After controls for repository traits, list count was the strongest README factor separating popular repos from zero-star repos. Popular repos averaged 3.4 lists; zero-star repos averaged 0.02 [Wang 2023].
- Give each section a heading that names its content so readers can jump to it. `count`: In a 20-person survey, 12 preferred a README with labeled sections for finding information [Prana 2019].
- Add a screenshot, diagram, or GIF when it shows output or setup faster than text. `corr`: Image links went with more stars [Liu 2022]. Image count had a medium effect alone and low importance after controls [Wang 2023], so rank images below lists and links.
- Add a badge when it carries information the reader needs, such as build status. `corr`, weak: Badges had a small effect alone and near-zero importance after controls [Wang 2023]. 85% of the Java repos had none [Liu 2022].
- Let length follow content. `corr`: Popular READMEs ran four times longer on average and length stayed significant after controls [Wang 2023]. Larger projects have more to document, so don't pad a small project's README to match.
- Update the README in the same change that alters install steps, usage, or links. `corr`: Update frequency ranked among the strongest factors [Wang 2023].

## Judgment rules

The skill's author wrote these. No study tested them.

- Skip the directory tree. Readers can browse the files, and a pasted tree goes stale.
- Link to the package manifest instead of copying the dependency list. The manifest stays current and a copy drifts.
- Move implementation detail into docs or subfolder READMEs. In a subfolder README, use a table with one line per file.
- Add a section when you have content for it. Skip placeholder sections.

## Steps

1. Read the manifest, entry points, existing README, LICENSE, and CONTRIBUTING files.
2. Compare the existing README with the Sections table. Note what is missing and what the judgment rules would cut.
3. Run the install and usage commands you document when the environment allows. Tell the user which ones you could not run.
4. Write or revise, applying the Format rules.
5. When you explain a choice to the user, name its tag. Describe `corr` findings as associations.

## Limits

- All four studies measured popularity through stars; one added forks, watchers, and pull requests. None measured whether readers understood or adopted a project faster.
- Liu 2022 checked timing in 182 repos. Stars rose after README changes in 106 and before them in 52. That favors READMEs helping without proving it.
- Liu 2022 studied Java alone. Wang 2023 compared repos with more than 100 stars against repos with zero, which widens the gap between groups.
