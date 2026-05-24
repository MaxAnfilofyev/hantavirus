# ANDV Swiss/Europe 2026 M516I Expert Handoff

## Why This Was Prepared

We are trying to make the public sequence data useful for qualified hantavirus/structural virology follow-up. This is not a claim of altered phenotype. It is a concise handoff of one molecular signal that survived local triage.

## Core Finding

The Andes virus M/GPC substitution `T516I` is rare in the Pathoplexus M-segment background but appears cleanly in three 2026 Europe/travel-cluster records. It is shared by Netherlands, Switzerland, and France records and is not unique to the Swiss sequence.

| Accession | Country | Date | aa516 | Codon | Notes |
|---|---|---|---|---|---|
| PP_006W6RC.2 | Netherlands | 2026-05-03 | I | ATA | ambiguous_M=0, unknown_M=0, completeness/length in metadata available |
| PP_006WBLH.2 | Switzerland | 2026-05-04 | I | ATA | ambiguous_M=0, unknown_M=0, completeness/length in metadata available |
| PP_006XBKH.1 | France | 2026-05-10 | I | ATA | ambiguous_M=0, unknown_M=0, completeness/length in metadata available |

## Frequency Context

- Full-length-ish M records: `I516` in 3/141 records in the first pass.
- All M records covering residue 516: `I516` in 3/148 records.
- Common background at 516 is threonine (`T`): 127/148 records covering the position.
- Other residues occur at low frequency (`K`, `X`, `S`, `W`, `F`) and should be treated cautiously without alignment/QC review.

## Structural Context

- Sequence scan: residue 516 lies near the `485-521` hydrophobic region and near the `N524` N-linked glycosylation motif.
- `T516I` increases local hydrophobicity around residue 516.
- AlphaFold Server: local CA pLDDT around residue 516 is moderate/useful (~79.8), but the broader chunk pTM is low, so global placement is not reliable.
- PDB/RCSB `9P3Y`: the ANDV Gn-Gc tetramer construct carries `T516`, but resolved Gn coordinates stop around residue 479. So 516 is in unresolved/membrane-proximal Gn territory in that structure.

## Haplotype Context

See `outputs/m_segment_haplotype_vs_swiss.csv` and `outputs/m_segment_2026_haplotypes.csv`. Initial result: the `I516` carrier records are protein-identical to the Swiss M sequence in this translated ORF comparison, i.e. `M516I` is part of the shared 2026 M protein haplotype rather than a Swiss-only singleton.

## Questions For A Hantavirus/Structural Virology Expert

1. In accepted ANDV GPC topology, does residue 516 fall in Gn ectodomain stem, membrane-proximal linker, transmembrane boundary, or cytoplasmic-facing territory?
2. Is the region around 485-521 known to affect Gn/Gc processing, trafficking, tetramer assembly, virion incorporation, or membrane fusion?
3. Does proximity to `N524` matter structurally or biosynthetically, even though `T516I` does not disrupt the `N524` glycosylation sequon?
4. Are any neutralizing antibodies known to bind near this unresolved Gn region, or is it unlikely to be antibody-accessible?
5. Does replacing threonine with isoleucine at 516 plausibly alter membrane association, local helix propensity, or glycoprotein maturation?
6. Would a T516/I516 pseudovirus or VLP comparison be straightforward, and which readout is most informative: incorporation, entry, fusion pH, or neutralization?
7. Is there any reason to prioritize this over other 9P3Y construct-vs-Swiss differences such as `K535V`, `I537V`, or Gc-side differences?

## Suggested Experiment

Matched T516 versus I516 GPC constructs in pseudovirus/VLP system: measure expression, processing, surface/virion incorporation, entry efficiency, fusion phenotype if available, and neutralization by ANDV antibodies or convalescent sera.

## Local Evidence Files

- `outputs/m516_all_pathoplexus_records_covering_position.csv`
- `outputs/m_segment_haplotype_vs_swiss.csv`
- `outputs/m_segment_2026_haplotypes.csv`
- `outputs/swiss_vs_9p3y_construct_differences.csv`
- `outputs/m516i_focused_note.md`