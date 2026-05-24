# M/GPC 516 Focused Note - ANDV 2026 Public Data

## Updated finding

After incorporating the Ghafari et al. Virological outbreak metadata, `M/GPC:T516I` should be framed as a shared Swiss-numbered M/GPC state in the non-Canadian outbreak-associated M records, not as a three-record subcluster mutation.

The correction matters because some public M consensus sequences are truncated or start-shifted. Directly reading raw ORF position 516 misclassifies several records. The updated tables translate each M ORF, align it to the Swiss full-length M/GPC protein, and then assign Swiss-numbered residue 516.

## Current status

- `PP_006WDKH.1`, the sampled-root-compatible sequence in Ghafari et al., maps to `M516I`.
- `PP_006W6RC.2`, discussed as a possible alternative/near-root sequence, also maps to `M516I`.
- Other non-Canadian Ghafari metadata records with usable M sequence also map to `M516I`.
- The two Canadian May 17 consensus records map to `X` at this residue in the local pull, consistent with unresolved/ambiguous sequence around this site.

## Structural context

Earlier structural triage remains useful but should be read as context only. `M516` lies near a hydrophobic/membrane-proximal Gn region and close in sequence to the `N524` glycosylation motif, without disrupting that motif. The corresponding region is not resolved in the public `9P3Y` ANDV Gn-Gc tetramer coordinates.

## Interpretation

This is a useful handoff item because it connects the Virological outbreak reconstruction to a protein/background-frequency annotation. It is not evidence by itself for changed phenotype. Follow-up would require expert review and, if warranted, matched `T516` versus `I516` GPC experiments such as pseudovirus/VLP incorporation, entry, processing/trafficking, or neutralization assays.
