# ANDV Swiss/Europe 2026 public-data triage

Informal public-data analysis of the MV Hondius / Swiss-resident 2026 Andes virus
sequence context, focused on whether any protein-level M/GPC signal deserves
expert follow-up.

## Main takeaway

The only protein-level signal that remained notable after Pathoplexus frequency,
codon, haplotype, and structural-context checks was `M/GPC:T516I`.

Current interpretation:

- `T516I` is cleanly supported as an `ATA` codon in the 2026 carrier records.
- It appears in Netherlands, Switzerland, and France 2026 records in this pull.
- It is rare in the Pathoplexus M-segment background but not Swiss-unique.
- It sits near a hydrophobic/membrane-proximal GPC region and near the `N524`
  glycosylation motif.
- It is not resolved in the public `9P3Y` ANDV Gn-Gc tetramer coordinates.
- This is a watch item or expert-review prompt, not evidence of altered
  phenotype.

No claim is made here about transmissibility, entry efficiency, antigenicity,
vaccine escape, clinical severity, or public-health risk.

## Suggested starting points

- `reports/andv_m516i_expert_handoff.md` - concise handoff for hantavirus GPC or
  structural virology experts.
- `reports/andv_swiss_2026_structural_triage_memo.md` - broader triage memo.
- `tables/m_segment_2026_haplotypes.csv` - 2026 M-protein haplotype summary.
- `tables/m516_all_pathoplexus_records_covering_position.csv` - all M records
  covering GPC residue 516 in this Pathoplexus pull.

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

