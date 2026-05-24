# Reconciliation with Ghafari et al. Virological outbreak reconstruction

Source compared: Virological thread `1037`, including the attached `Hanta_metadata_outbreak_sequences.csv`, against the local Pathoplexus pull and the previously generated M/GPC context tables. Residue calls below are mapped to the Swiss full-length M/GPC numbering, because several outbreak consensus M segments are truncated or start-shifted and cannot be interpreted by raw ORF position alone.

## Main result

In the eight outbreak-associated records listed in the Ghafari metadata file, the Swiss-numbered M/GPC residue 516 state is: `{'I': 6, 'X': 2}`. The proposed sampled root sequence `PP_006WDKH.1` maps to `M516I` (`ATA`), and the alternative/near-root candidate discussed in the post, `PP_006W6RC.2`, also maps to `M516I` (`ATA`). The two Canadian May 17 consensus records map to `X` at this residue in this pull because the local consensus region is unresolved/ambiguous around the mapped position.

`M/GPC:T516I` should therefore be described differently than in the earlier draft: it is not merely a three-record subcluster signal. It appears to be the shared mapped M/GPC 516 state across the non-Canadian outbreak-associated M records in the Ghafari metadata set. In this local pull, the mapped `M516I` carriers in/near the Ghafari set are: `PP_006W3U9.2, PP_006W6RC.2, PP_006WBLH.2, PP_006WDJK.1, PP_006WDKH.1, PP_006XBKH.1`.

## Relationship to the Virological post

Ghafari et al. focused on candidate differences **within** the sampled outbreak consensus sequences after manual masking of terminal/indel-associated sites. Their statement that resolved coding-region differences were synonymous is compatible with this result if the non-Canadian outbreak records share the same M/GPC 516 state. Our updated note is therefore not a contradiction; it is an annotation of the outbreak M/GPC state against broader ANDV M-segment background.

The reconciliation changes the handoff wording:

- Do not imply that `T516I` separates the non-Canadian outbreak sequences from each other.
- Do not imply disagreement with the Virological rooting analysis.
- Say that the proposed root (`WDKH.1`) and possible alternative/near-root (`W6RC.2`) both map to `M516I`.
- Treat the Canadian records carefully because the Virological post notes updated versions and residual divergence/ambiguity, and the May 17 consensus records map as unresolved at this residue.

## What this advances without lab access

The metadata lets us separate three questions that were previously blurred:

1. Is `M516I` Swiss-only? No.
2. Is `M516I` a within-outbreak discriminator among non-Canadian records? No.
3. Is `M516I` an outbreak/background protein annotation worth checking with GPC/entry experts? Yes, because it is shared by the proposed sampled root and the non-Canadian outbreak M records while remaining uncommon in the broader mapped Pathoplexus M set.

That is enough to justify expert review as a **protein/background-frequency annotation attached to the outbreak reconstruction**, not as a claim about entry, transmissibility, antigenicity, virulence, or vaccine relevance.

## Files

- `tables/ghafari_outbreak_m516_reconciliation.csv`
- `tables/ghafari_outbreak_m_protein_vs_wdkh1.csv`
- `tables/m516_swiss_numbered_pathoplexus_records.csv`
