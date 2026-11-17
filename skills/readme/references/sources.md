# Sources

Each entry lists what the study measured and the numbers the skill uses. On 2026-11-17, Claude (Opus 5.5) read the full text of each paper, matched each number to its table or section, and checked each DOI against Crossref.

## Prana 2019

Prana, G. A. A., Treude, C., Thung, F., Atapattu, T., and Lo, D. Categorizing the content of GitHub README files. *Empirical Software Engineering* 24(3), 1296–1327, 2019. [doi:10.1007/s10664-018-9660-3](https://doi.org/10.1007/s10664-018-9660-3). Preprint: [arXiv:1802.06997](https://arxiv.org/abs/1802.06997).

- **Sample:** 4,226 sections from 393 randomly selected GitHub READMEs, labeled by hand.
- **Measured:** What READMEs contain. No popularity or outcome measure.
- **Numbers used (Table 3):** "What" content in 97.0% of files, "How" in 88.5%, "Why" in 25.7%, "Contribution" in 27.8%.
- **Survey (Section 6.7):** 20 software professionals from Mechanical Turk compared a README with section labels against one without. 12 preferred the labeled version, 6 were neutral, 2 preferred the unlabeled one.
- **Limits:** The survey is small. The claim that a "Why" section helps a project stand out is the authors' argument (Section 7), not a measured result.

## Liu 2022

Liu, Y., Noei, E., and Lyons, K. How ReadMe files are structured in open source Java projects. *Information and Software Technology* 148, 106924, 2022. [doi:10.1016/j.infsof.2022.106924](https://doi.org/10.1016/j.infsof.2022.106924). Preprint: [PDF](https://enoei.github.io/papers/liu2022readme.pdf).

- **Sample:** 14,901 Java repositories on GitHub; 11,594 English READMEs for the section analysis.
- **Measured:** Stars, compared between repos with and without each GitHub-recommended section (Mann–Whitney U, Cohen's d).
- **Numbers used (Table 3):**

  | Section | Share of READMEs | Cohen's d |
  |---------|------------------|-----------|
  | License | 13% | 0.416 |
  | Contributing | 5% | 0.415 |
  | Usage | 31% | 0.314 |
  | Installation | 21% | 0.311 |
  | Credits | 4% | 0.287 |
  | Table of contents | 2% | 0.219 |
  | Description | 41% | 0.039 |

- **Other findings:** READMEs with a project name, usage, installation, license, code snippets, or image links went with more stars (abstract). More than 85% of repos had no badges (Section 3).
- **Timing check (Section 4.1):** A Granger test on 182 repos found stars rose after README section changes in 106 (58.2%) and before them in 52 (29.1%).
- **Limits:** Java only (Section 4.2). Correlational.

## Wang 2023

Wang, T., Wang, S., and Chen, T.-H. Study the correlation between the readme file of GitHub projects and their popularity. *Journal of Systems and Software* 205, 111806, 2023. [doi:10.1016/j.jss.2023.111806](https://doi.org/10.1016/j.jss.2023.111806). Preprint: [PDF](https://petertsehsun.github.io/papers/jss_2023_readme.pdf).

- **Sample:** 5,000 GitHub repositories in more than 20 languages. 756 popular (more than 100 stars) and 810 non-popular (zero stars).
- **Measured:** README features compared between groups (Wilcoxon rank-sum, Cliff's δ), then a random forest that controls for repository traits such as license, language, and tags.
- **Numbers used (Table 4, mean popular vs. zero-star):**

  | Feature | Popular | Zero-star | Cliff's δ |
  |---------|---------|-----------|-----------|
  | Links | 43.5 | 5.3 | 0.67 (large) |
  | Length (characters) | 12,396 | 3,116 | 0.63 (large) |
  | Images | 4.3 | 0.8 | 0.41 (medium) |
  | Lists | 3.4 | 0.02 | 0.39 (medium) |
  | Code blocks | 6.2 | 2.3 | 0.26 (small) |
  | Badges | 1.1 | 0.14 | 0.26 (small) |

- **After controls (Table 6):** List count ranked third of all factors and first among README factors. Update count, update interval, length, and link count stayed significant. Images and badges ranked near the bottom.
- **Updates (RQ3):** Popular repos spent the largest share of README updates (47%) on references. Zero-star repos spent the largest share (34%) on usage content.
- **Limits:** The zero-vs-100-star split widens the gap between groups (Section 5.3). The authors state they cannot conclude causation.

## Venigalla 2022

Venigalla, A. S. M., and Chimalakonda, S. An empirical study on correlation between readme content and project popularity. [arXiv:2206.10772](https://arxiv.org/abs/2206.10772), 2022. Not peer reviewed.

- **Sample:** 1,950 READMEs across ten languages. For each language, the top 100 and bottom 100 repos by a combined rank of stars, forks, watchers, and pull requests.
- **Measured:** README features and content categories compared between groups (Wilcoxon rank-sum, Fisher's exact test), then a random forest.
- **Findings used:** Popular projects organized READMEs with lists and images, linked to external sources, and included contribution guidelines and references more often. Usage content appeared in most READMEs regardless of popularity.
- **Limits:** Preprint. The abstract describes popular READMEs; it does not compare lists against prose or mention badges. Correlational.
