# ANDV 2026 M/GPC 516 Expert Handoff

## Short version

Public-data reconciliation against the Ghafari et al. Virological outbreak metadata suggests that Swiss-numbered `M/GPC 516I` is shared by the non-Canadian May 2026 outbreak-associated M records in the local Pathoplexus pull, including the proposed sampled root `PP_006WDKH.1` and the possible alternative/near-root `PP_006W6RC.2`. The two Canadian May 17 consensus records map as unresolved/ambiguous at this residue in this pull.

This supersedes an earlier raw-ORF-position pass that undercounted `516I` carriers because several M consensus records are truncated or start-shifted. Residue calls here are mapped by aligning translated M ORFs to the Swiss full-length M/GPC sequence before assigning Swiss-numbered residue 516.

## Why an expert might care

This is not a within-outbreak discriminator among the non-Canadian records. Its value is as a protein/background annotation: the outbreak-associated M records share an `I` state at a membrane-proximal/unresolved Gn-region position where most broader mapped Pathoplexus M records carry `T`.

Current mapped frequency in this pull:

- All mapped M records: `T=133`, `I=7`, `X=4` across 144 records.
- Full-length-ish M records (`completeness_M >= 0.9`): `T=129`, `I=6`, `X=1` across 136 records.

## Interpretation boundary

No claim is made that `M/GPC:T516I` changes transmissibility, virulence, receptor usage, entry efficiency, antigenicity, vaccine escape, diagnostic escape, or clinical risk. Other Virological analyses report near-identity of S/M consensus sequences in the early outbreak set, no detected reassortment among sampled lineages, no elevated molecular clock rate leading to the outbreak lineage, and no evidence for human-associated adaptation in a preliminary GPC selection analysis. The strongest defensible statement is that this is an outbreak/background glycoprotein-state annotation worth quick review by ANDV GPC/entry or structural virology experts.

## Files

- `reports/ghafari_outbreak_reconciliation.md`
- `tables/ghafari_outbreak_m516_reconciliation.csv`
- `tables/m516_swiss_numbered_pathoplexus_records.csv`
- `tables/pathoplexus_position_frequencies.csv`
