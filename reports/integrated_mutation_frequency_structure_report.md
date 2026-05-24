# Integrated Mutation/Frequency/Structure Report - Updated

## Main update

The Ghafari et al. Virological metadata changed the interpretation of `M/GPC:T516I`. A raw ORF-position method undercounted carriers because multiple outbreak M consensus sequences are truncated or start-shifted. The updated method maps translated M ORFs to the Swiss full-length M/GPC sequence before assigning Swiss-numbered residue 516.

## Swiss-numbered M516 frequency

- All mapped M records: `T=133`, `I=7`, `X=4` across 144 records.
- Full-length-ish M records (`completeness_M >= 0.9`): `T=129`, `I=6`, `X=1` across 136 records.

In the Ghafari May 17 outbreak metadata set, the six non-Canadian records map to `M516I`; the two Canadian May 17 consensus records map to `X` at this residue in this pull.

## Relationship to outbreak reconstruction

This does not contradict Ghafari et al.'s statement that resolved within-outbreak coding-region differences were synonymous. The non-Canadian outbreak records share the same mapped residue 516 state. The useful contribution is a background-frequency and structural-context annotation for the outbreak M/GPC state.

## Structure context

`M516` is near a hydrophobic/membrane-proximal Gn region and close to the intact `N524` glycosylation motif. It is not resolved in public `9P3Y` coordinates. This supports expert-review triage, not phenotype inference.

## Files

- `reports/ghafari_outbreak_reconciliation.md`
- `tables/ghafari_outbreak_m516_reconciliation.csv`
- `tables/m516_swiss_numbered_pathoplexus_records.csv`
- `tables/pathoplexus_position_frequencies.csv`
