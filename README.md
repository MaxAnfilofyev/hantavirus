# ANDV Swiss/Europe 2026 public-data triage

Informal public-data analysis of the MV Hondius / Swiss-resident 2026 Andes virus
sequence context, focused on whether any protein-level M/GPC annotation deserves
expert follow-up.

## Main takeaway

The main protein-level handoff item is Swiss-numbered `M/GPC 516`.

Current interpretation:

- After reconciliation with the Ghafari et al. Virological outbreak metadata,
  the non-Canadian outbreak-associated M records map to `M516I`.
- The proposed sampled root sequence `PP_006WDKH.1` and possible alternative or
  near-root sequence `PP_006W6RC.2` both map to `M516I`.
- The two Canadian May 17 consensus records map as unresolved at this residue in
  this pull.
- `M516I` is uncommon in the broader mapped Pathoplexus M-segment background but
  is not Swiss-unique.
- It sits near a hydrophobic/membrane-proximal GPC region and near the `N524`
  glycosylation motif.
- It is not resolved in the public `9P3Y` ANDV Gn-Gc tetramer coordinates.
- This is a watch item or expert-review prompt, not evidence of altered
  phenotype.

No claim is made here about transmissibility, entry efficiency, antigenicity,
vaccine escape, clinical severity, or public-health risk.

## Suggested starting points

- `reports/virological_thread_findings_review.md` - cross-check against other
  Virological Hantavirus analysis threads.
- `reports/ghafari_outbreak_reconciliation.md` - reconciliation against the
  Virological outbreak metadata and rooting discussion.
- `reports/andv_m516i_expert_handoff.md` - concise handoff for hantavirus GPC or
  structural virology experts.
- `reports/andv_swiss_2026_structural_triage_memo.md` - broader triage memo.
- `tables/m_segment_2026_haplotypes.csv` - 2026 M-protein haplotype summary.
- `tables/m516_swiss_numbered_pathoplexus_records.csv` - M records with residue
  516 assigned by mapping translated M ORFs to the Swiss full-length M/GPC
  sequence.

## Data sources

- Swiss FASTA originally shared on Virological.org:
  `sequences/ANDV-Switzerland-Hu-3337-2026.fasta`
- Pathoplexus ANDV LAPIS API:
  `https://lapis.pathoplexus.org/andv/sample/details`
  and
  `https://lapis.pathoplexus.org/andv/sample/unalignedNucleotideSequences?versionStatus=LATEST_VERSION`
- RCSB PDB `9P3Y` mmCIF was used locally for construct/coordinate context.

## AlphaFold notice

This repository does not redistribute AlphaFold Server raw outputs, including
model CIF files, ZIP downloads, PAE/contact-probability arrays, full prediction
JSON, or screenshots. Some qualitative structural comments were informed by
locally generated AlphaFold Server predictions; see `NOTICE.md`.

## Intended use

This is a rapid, informal research note for non-commercial scientific discussion.
It is not clinical, diagnostic, therapeutic, or public-health guidance.
