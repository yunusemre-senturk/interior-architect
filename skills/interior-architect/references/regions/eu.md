# European Union (general)

**Status: skeleton. Codes are national, not EU-wide.** Use this file only as a pointer, and tell the user that their national code was not checked. When a country file exists (for example `de.md`), use it instead.

## Electrical
- National codes are based on IEC 60364 / HD 60364. The bathroom part is 701, for example DIN VDE 0100-701 in Germany. France uses NF C 15-100, which has its own "volumes" rules. The zone idea is the same everywhere; check the national details.
- 30 mA RCDs on bathroom circuits are near-universal.

## Gas
- Gas installation rules are national, and the work needs a certified installer.

## Kitchen planning
- Some countries have kitchen planning standards, for example DIN 18011 in Germany (verify).
- Counters are commonly around 90 cm high.

## Contributing
Add `regions/<iso-code>.md` with: status line, regulations (R), gas, electrical, ventilation, market practice, local terms, sources. Follow the format of `tr.md`.
