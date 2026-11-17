# research-backed-skills

This repo contains agent skills with actual studies to back them up. If you want skills built on my personal tastes, please see [taste-skills](https://github.com/JohnVonDrashek/taste-skills).

## Why

Because most skills are just people asking AI to write skills, which is pointless and a waste of time. These ones actually use studies to make skills.

## Skills

| Skill | What it does |
|-------|--------------|
| [readme](skills/readme/SKILL.md) | Writes, revises, or trims a README using four studies of GitHub READMEs |

## Evidence tags

Each rule carries a tag so you can see how much weight it holds:

- `exp`: a controlled experiment tested it. No rule has one yet.
- `corr`: a peer-reviewed study linked it to a better outcome, like more GitHub stars. You can't tell from the study which came first.
- `count`: a study counted how often READMEs do it. It didn't measure whether that helps.
- `judgment`: no study backs it. The rule gives its reason so you can disagree.
- `preprint`: sits next to another tag when the authors posted the study without peer review.

Each skill folder has a `references/sources.md` with the sample, method, numbers, and limits of each study it cites. Start with [the readme skill's sources](skills/readme/references/sources.md).

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
