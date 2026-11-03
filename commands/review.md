---
description: Critique an existing plan, drawing, photo or idea like a senior interior architect
argument-hint: "[file path, image, or description of the design]"
---
Use the interior-architect skill. Review this design: $ARGUMENTS

Delegate to the `design-critic` agent with the design and the brief (house rules, design log, region). If agents are not available, do the review yourself in the same order: constraints, safety and systems, ergonomics and circulation (doors open), `references/detail-checklist.md`, light / acoustics / wellbeing, aesthetics, missed opportunities, unverified numbers.

Return a ranked list (blocker / major / minor / opportunity) with a concrete fix for each, numbers tagged V / R / G, and a one-line verdict.
