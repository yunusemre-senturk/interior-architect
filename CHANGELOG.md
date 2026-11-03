# Changelog

## 0.2.0 - 2026-11-04
Research-driven upgrade: the knowledge base was extended from ~25 web sources read with Firecrawl (Terrapin, OSHA, WELL / IES, CPSC, RIBA, TMMOB İçmimarlar Odası, Planlı Alanlar İmar Yönetmeliği, peer-reviewed research and practice guides).

### Added
- **Agents:** `design-critic` (fresh-eyes ranked critique) and `precedent-researcher` (precedents, products, current guidance; prefers Firecrawl).
- **Slash commands:** `brief`, `survey`, `concept`, `review`, `palette`, `budget`, `research`, `snag`.
- **References:** `design-process.md`, `discovery-brief.md`, `innovation-playbook.md`, `detail-checklist.md`, `wellbeing.md`, `acoustics.md`, `furnishing-styling.md`, `accessibility-family.md`, `home-office-small-spaces.md`, `stairs.md`, `sustainability.md`, `project-delivery.md`.
- **Templates:** brief questionnaire, concept board, budget sheet, snag list.
- **Evals:** scenarios 11-18 (living room, wall bed office, ageing parents, toddler safety, budget, flawed-plan review, circadian light, echo).
- README redesign with banner, badges, workflow diagram; Turkish README in parity.

### Changed
- `SKILL.md`: senior-designer mindset ("think in four dimensions", "invent, then test", "sweat the details"), a sixth lens (**wellbeing**), project-stage awareness, reference map, new gotchas.
- `lighting.md`: downlight spacing and circadian targets.
- `regions/tr.md`: stairs (Art. 31), kitchen hood flue (Art. 34), TMMOB İçmimarlar Odası service phases, stronger earthquake anchoring guidance; sources checked 2026-11.
- `sources.md`: every new number traced to a source.

## 0.1.0 - unreleased
- First public version, generalized from a private Turkish skill (`ic-mimar`).
- Short `SKILL.md` with the workflow and the five lenses. Room-by-room detail moved into `references/`.
- Region files: `tr` full; `us`, `uk` and `eu` as skeletons.
- Personal standing corrections replaced by a private house-rules mechanism with anonymous examples.
- Fallbacks for hosts that do not offer Projects, canvases or prompt-sending widgets.
- Assets: templates for house rules and the design log, a survey sheet, and the configurator.
- Ten eval scenarios, plus a privacy check to run before each release.
