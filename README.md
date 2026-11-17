# research-backed-skills

This repo contains agent skills with actual studies to back them up. If you want skills built on my personal tastes, please see [taste-skills](https://github.com/JohnVonDrashek/taste-skills).

## Why

Because most skills are just people asking AI to write skills, which is pointless and a waste of time. These ones actually use studies to make skills.

## Skills

| Skill | What it does |
|-------|--------------|
| [readme](skills/readme/SKILL.md) | Writes, revises, or trims a README using four studies of GitHub READMEs |

## Evidence Tags

Tags give you insight into how and why a rule became a rule and to give disclosures about the rule:

- `exp`: rule was tested in a controlled experiment
- `corr`: how much a rule correlated with a better outcome
- `count`: how often READMEs do it
- `judgment`: indicates what judgment calls were made to make the skill functional
- `preprint`: indicates the authors posted the study without peer review

Each skill folder has a `references/sources.md` if you want to see how studies contributed to the making of the skill.

## Install

1. Clone the repo:

   ```bash
   git clone https://github.com/JohnVonDrashek/research-backed-skills.git ~/code/research-backed-skills
   ```

2. Link the skill into your Claude Code skills folder:

   ```bash
   mkdir -p ~/.claude/skills
   ln -s ~/code/research-backed-skills/skills/readme ~/.claude/skills/readme
   ```

Run `git pull` in the clone to get updates.

## Use

In Claude Code, type `/readme` or ask in plain words:

```text
write a README for this project
cut this README down to what it needs
```

Claude reads your manifest and docs and skips any section it would have to guess at. When it explains a choice, it names the tag behind it.

## Contributing

New rules need a tag and a sources entry, and you check each DOI against Crossref. [CONTRIBUTING.md](CONTRIBUTING.md) has the full standard.

## License

[MIT](LICENSE)
