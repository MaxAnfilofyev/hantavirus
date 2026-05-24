# ANDV Swiss 2026 Structural Triage Memo

## Executive Takeaway

This analysis is not duplicating vaccine design work. It is a public-sequence structural triage. The Swiss/travel-cluster ANDV proteins are very close to existing Pathoplexus ANDV references. The only protein difference that remains worth flagging after frequency and structure checks is `M/GPC:T516I`. It is cleanly supported and rare in Pathoplexus, but current public sequence plus AlphaFold evidence is not sufficient to infer altered entry, immune escape, transmissibility, or vaccine impact.

## What Was Compared

- Swiss 2026 FASTA: local `ANDV-Switzerland-Hu-3337-2026.fasta`.
- Public reference set: Pathoplexus ANDV LAPIS metadata and latest unaligned nucleotide FASTA.
- Structural sources: AlphaFold Server predictions generated in this workflow, plus RCSB/PDB `9P3Y` ANDV Gn-Gc tetramer/Fab mmCIF downloaded locally.

## Protein-Level Differences Versus Close Older Reference

Closest older reference used for first-pass mutation table: `PP_006VZ4W.1` / Argentina family.

| Segment | Differences | Interpretation |
|---|---|---|
| L/polymerase | `V70I`, `K144R` | Both Swiss residues are common in Pathoplexus full-length L records and high-confidence in AlphaFold. Not notable alone. |
| S/nucleocapsid | none | Protein-identical versus the selected close older reference. |
| M/GPC | `T193A`, `T516I` | `T193A` is common. `T516I` is rare and outbreak-associated. |

## M516I Frequency and Codon Support

Among all Pathoplexus M records whose translated ORF covers residue 516, counts are: {'T': 127, 'S': 3, 'W': 3, 'X': 4, 'K': 6, 'F': 2, 'I': 3}.

| Accession | Country | Date | aa516 | codon516 | completeness_M | ambiguous_M | unknown_M |
|---|---|---|---|---|---:|---:|---:|
| PP_006W6RC.2 | Netherlands | 2026-05-03 | I | ATA | 0.9874693543993462 | 0 | 0 |
| PP_006WBLH.2 | Switzerland | 2026-05-04 | I | ATA | 0.9940070825388178 | 0 | 0 |
| PP_006XBKH.1 | France | 2026-05-10 | I | ATA | 0.9942794878779624 | 0 | 0 |

All `I516` carriers use codon `ATA` and have zero ambiguous/unknown M nucleotides in the downloaded Pathoplexus metadata. So this is not an ambiguity-driven translation artifact in the records checked.

## Structure and Topology Evidence

- GPC sequence scan places a hydrophobic region at roughly `485-521`; `T516I` falls near the end of that hydrophobic region.
- `N524` is an N-linked glycosylation motif and is nearby in sequence. `M516I` does not remove the `N524` motif.
- AlphaFold residue-level confidence at GPC 516 is moderate/useful: CA pLDDT about `79.8` in `M_glycoprotein_precursor_chunk02_aa351-800`.
- The broader AlphaFold chunk containing 516 has low global pTM (`0.43`), so local residue confidence is more useful than the global fold placement.
- PDB `9P3Y` contains the ANDV Gn-Gc tetramer/Fab construct with reference `T516`, but resolved Gn coordinates cover roughly residues `20-479`; residue 516 is present in construct sequence but not resolved in the coordinates.

Interpretation: M516 is best treated as membrane-proximal/unresolved Gn territory in the current public structural evidence. It is not a clean, resolved, antibody-facing epitope from `9P3Y`.

## Swiss 2026 Versus 9P3Y Construct

The Swiss GPC differs from the 9P3Y construct core at 12 protein positions in this extraction. Differences include:

| Region | GPC position | 9P3Y aa | Swiss aa | Difference |
|---|---:|---|---|---|
| Gn_9P3Y_entity3 | 8 | V | A | V8A |
| Gn_9P3Y_entity3 | 114 | I | V | I114V |
| Gn_9P3Y_entity3 | 294 | H | Y | H294Y |
| Gn_9P3Y_entity3 | 346 | V | I | V346I |
| Gn_9P3Y_entity3 | 353 | T | V | T353V |
| Gn_9P3Y_entity3 | 516 | T | I | T516I |
| Gn_9P3Y_entity3 | 535 | K | V | K535V |
| Gn_9P3Y_entity3 | 537 | I | V | I537V |
| Gc_9P3Y_entity4_core | 1023 | T | A | T1023A |
| Gc_9P3Y_entity4_core | 1055 | S | T | S1055T |
| Gc_9P3Y_entity4_core | 1096 | L | S | L1096S |
| Gc_9P3Y_entity4_core | 1127 | V | I | V1127I |

This matters because 9P3Y is a structural reference, not an exact Swiss/outbreak sequence match. `T516I` is one of several differences, but it is the one that stood out as rare in the broader Pathoplexus background.

## What Can Be Said

- `M516I` is a clean, rare, 2026-cluster-associated GPC substitution.
- It increases local hydrophobicity around residue 516.
- It lies near the `485-521` hydrophobic region and near, but not disrupting, the `N524` glycosylation motif.
- It is not unique to Switzerland; it is shared by Netherlands, Switzerland, and France 2026 records in this Pathoplexus pull.

## What Cannot Be Said

- No evidence here that `M516I` changes transmissibility.
- No evidence here that it changes receptor usage or entry efficiency.
- No evidence here that it creates antibody escape or vaccine escape.
- No evidence here that it is clinically meaningful.

## Experimental Follow-Up

The right wet-lab comparison is a matched `T516` versus `I516` GPC experiment: pseudovirus or VLP incorporation, entry efficiency, Gn/Gc processing/trafficking, and neutralization by known ANDV antibodies or convalescent sera. Without that, `M516I` should remain a watch item, not a conclusion.

## Local Artifacts

- `outputs/m516_all_pathoplexus_records_covering_position.csv`
- `outputs/swiss_vs_9p3y_construct_differences.csv`
- `outputs/m516i_focused_note.md`
- `outputs/integrated_mutation_frequency_structure_report.md`