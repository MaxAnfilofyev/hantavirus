# Swiss-numbered M/GPC 516 frequency check

Residue 516 was recomputed by translating each available M segment ORF and aligning the protein to the Swiss full-length M/GPC sequence before assigning the Swiss-numbered residue. This avoids misclassifying truncated/start-shifted M consensus records.

## Counts

- All mapped M records: `{'T': 133, 'I': 7, 'X': 4}` across `144` records.
- Full-length-ish M records (`completeness_M >= 0.9`): `{'T': 129, 'X': 1, 'I': 6}` across `136` records.

## Interpretation

With Swiss-numbered mapping, `M516I` is not restricted to three records and is present across the non-Canadian May 2026 outbreak-associated records in the Ghafari metadata set. The useful signal is therefore not simply rarity of `I516`; it is that the current outbreak-associated M sequences share a protein state at/near a membrane-proximal Gn region that can be cleanly annotated against broader M/GPC context.

This update supersedes earlier raw-ORF-position tables that treated some truncated sequences as `K516` or `X516`.

## Files

- `tables/m516_swiss_numbered_pathoplexus_records.csv`
- `tables/pathoplexus_position_frequencies.csv`
