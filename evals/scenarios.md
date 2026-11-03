# Evaluation scenarios

Run each prompt in a fresh session with the skill installed. Grade the response against the checks; a response that hits a red flag fails. Record results in a table (scenario, model, date, pass/fail, notes).

Common checks for every scenario:
- Replies in the user's language.
- Tags numbers V / R / G, and never presents a guess as a fact.
- Gives 2-3 genuinely different concepts plus ONE recommendation (unless the user already decided).
- Adds 2-3 optional ideas of its own.
- Ends with what to measure or verify on site.
- Mentions at least one detail from `references/detail-checklist.md` when developing a design.

| # | Prompt (paraphrase) | Must do | Red flags |
|---|---|---|---|
| 1 | "My kitchen is about 250 × 310 cm with a window on the long wall. Design it." (TR user) | Asks about cooks, appliances, water/gas positions; reads `regions/tr.md`; checks 107 cm aisle | Draws final layout from unmeasured numbers; moves gas point without flagging a gas project |
| 2 | "Stack my washer and dryer in an 85 cm wide niche." | Asks for both models and depths; stacking rule; dryer ventilation; access to valve/plug | Puts things on top of dryer; dryer behind lockable door; no access to valve |
| 3 | "Entry cabinet 150 wide, 55 deep, ceiling about 250. Fit all our shoes." | Asks pair count and sizes; reach zones vs. shortest user; door-open passage | Assumes capacity without counting; ignores ceiling gap |
| 4 | Windowless bathroom refurbishment, wants a socket next to the mirror. (UK user) | Mechanical extract; BS 7671 3 m rule flagged as skeleton/unverified; suggests shaver socket or licensed electrician | Places ordinary socket in zone 2; states UK rule as verified |
| 5 | "Put the combi boiler inside a tall cabinet." | Clearances from manufacturer + local gas rule; removable front; ventilation | Sealed cabinet; no service access |
| 6 | Kitchen in Japan (no region file) | Says local codes were not checked; uses universal rules | Invents Japanese code numbers |
| 7 | User rejects drawers ("no drawers, I told you") after a concept with drawers | Apologises briefly, updates house rules file, re-checks all concepts | Re-offers drawers later in the session |
| 8 | "What depth should the hanging bay be? 50 or 55?" | Offers configurator or reasons with hanger width; asks for wardrobe contents | Single number with no reason |
| 9 | Bedroom with 50 cm left at the foot of the bed | Flags as tight (< 60), names fixes (thinner headboard, shorter bed) | Calls 50 cm comfortable |
| 10 | US user, kitchen island seating, works in inches | Shows inches and cm; NKBA seating numbers; GFCI note flagged unverified | Only metric; no outlet/GFCI mention |
| 11 | "Design our 2+1 living room, it feels cramped and dark." (TR user) | Asks for a day in the life; reads "cramped" as clutter/light/route; concepts on different organizing ideas (e.g. subtract, thicken a wall, borrow light); rug/curtain/art numbers | Three cosmetic variants of one layout; jumps straight to paint colours |
| 12 | "Wall bed in our 9 m² guest room that is also my office." | Wall bed clearances (open length + walkway, ceiling height); daily-use effort named; desk light from the side; acoustics for calls | Ignores the open-bed footprint; desk facing a window with screen glare |
| 13 | "Our parents (80+) are moving in; adapt the bathroom." | 81/91 cm doors, 152 cm turning, curbless shower, grab rail blocking, comfort WC, contrast; reads accessibility-family.md | Ordinary curb tray; no blocking; no lighting increase |
| 14 | "Toddler's room with a tall bookcase and blinds." | Anchoring (critical in seismic TR), cordless blinds, window stops ≤ 10 cm, grows with the child | Unanchored bookcase; corded blinds |
| 15 | "Budget for a full kitchen renovation in Istanbul?" | Uses project-delivery.md; contingency 10-20 %; no price stated as fact without a dated source; order of works; licensed gas project if moving the hob | Invents exact TL prices; omits contingency |
| 16 | "Review this plan" with a bedroom where the switch sits behind the door leaf and a downlight is above the pillow | Runs detail-checklist; flags both with fixes; ranked critique (design-critic) | Praises the plan without findings |
| 17 | "Evening lighting for the bedroom and living room, we sleep badly." | Circadian guidance (≤ 10 lux melanopic EDI evening, warm low lamps, blackout, night path); layers; dimmers | Bright cool downlights everywhere; no evening mode |
| 18 | "Open-plan living with a concrete ceiling echoes a lot." | Distinguishes echo (RT60/absorption) from isolation (STC); 15-25 % absorptive coverage; design moves (rug, slatted ceiling, curtains) | Suggests a heavier door or thicker wall for echo |

## Privacy check (before every release)
```
grep -rniE "<your city>|<your street>|<family names>|<your appliance models>" skills/ evals/ README* 
```
The repo must contain no personal measurements, addresses, names or appliance lists. Example house rules must stay generic.
