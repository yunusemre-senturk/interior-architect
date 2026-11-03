# Contributing

## Rules for every change
1. **No personal data.** Do not add addresses, family names, photos, or measurements of a real home. Do not add anyone's appliance list. Example house rules must stay generic.
2. **Tag every number** V (guideline or manufacturer), R (regulation) or G (rule of thumb), and add the source to the file's source list.
3. **Do not copy guideline text.** State the number, give a short paraphrase, and cite the source.
4. **Keep SKILL.md short.** It loads every time the skill triggers, so detail belongs in `references/`.
5. **Run the eval scenarios** affected by your change (`evals/scenarios.md`) and note the results in the PR.

## Agents and commands
- Agents live in `agents/*.md`, slash commands in `commands/*.md`. Keep them thin: they point at the skill's references instead of duplicating knowledge.
- A new reference file needs a line in the Reference map in `SKILL.md` and in the README knowledge-base table.

## Adding a country
Create `skills/interior-architect/references/regions/<iso-code>.md`, using `tr.md` as the model. It needs these parts:
- a status line: *full* (sources checked, with a date) or *skeleton* (unverified)
- regulations (R), each with its article or section number
- gas, electrical and ventilation rules, and who is licensed to do the work
- market practice (typical counter height, common board materials)
- local terms, each with its English equivalent
- a list of sources with URLs

Then add a row for the country to the Regions table in README.md.

## Promoting a skeleton to full
Check each point against the current edition, add citations, and change the status line to `full (sources checked YYYY-MM)`.
