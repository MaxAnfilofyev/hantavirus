# Mutation and Structure Annotation - ANDV Swiss 2026

Input mutations are Swiss 2026 protein differences versus close older Pathoplexus reference `PP_006VZ4W.1`. AlphaFold confidence is from the top-ranked local model covering each residue.

- M/GPC length: 1138 aa
- WAASA motif starts at M aa 647; cleavage is expected around this conserved motif, separating Gn-like N-terminal and Gc-like C-terminal regions.
- N-linked glycosylation motifs in M/GPC: 138:NQT, 350:NHS, 402:NIS, 524:NES, 930:NLT
- Hydrophobic transmembrane-like windows by simple KD scan: 148-166 maxKD=1.63, 485-521 maxKD=2.42, 628-652 maxKD=2.02, 1097-1133 maxKD=3.51

| Segment | Mutation | Region | AF job | CA pLDDT | Nearby N-glyc motif | Nearby hydrophobic region | Initial interpretation |
|---|---|---|---|---:|---|---|---|
| L | V70I | N-terminal L/polymerase region; outside the stronger central polymerase chunk in this first-pass model | andv_swiss_2026_l_polymerase_chunk01_aa1_650 | 93.34 | none | none | High-confidence N-terminal polymerase substitution in this model; conservative/non-obvious functional signal without external motif evidence. |
| L | K144R | N-terminal L/polymerase region; outside the stronger central polymerase chunk in this first-pass model | andv_swiss_2026_l_polymerase_chunk01_aa1_650 | 92.95 | none | none | High-confidence N-terminal polymerase substitution in this model; conservative/non-obvious functional signal without external motif evidence. |
| M | T193A | Gn ectodomain/head/base region before WAASA cleavage | andv_swiss_2026_m_glycoprotein_precursor_chunk01_aa1_450 | 89.81 | none | none | High-confidence Gn-side substitution; not near WAASA, not in a predicted hydrophobic/TM stretch, and not within 10 aa of an N-glycosylation motif by this scan. |
| M | T516I | Gn ectodomain/head/base region before WAASA cleavage | andv_swiss_2026_m_glycoprotein_precursor_chunk02_aa351_800 | 79.81 | N524NES | none | Moderate-confidence Gn-side substitution near the glycoprotein middle/TM-proximal region; in the lower-confidence chunk02 context, so structural placement is less reliable than M193. |

## Bottom line

The protein-level differences versus the close older Argentina reference are sparse and do not create an obvious AlphaFold-supported red flag. `M:T193A` is the cleanest interpretable glycoprotein change and appears structurally well-modeled. `M:T516I` is potentially more interesting because it lies in the middle Gn-side/proximal region, but AlphaFold confidence around the broader chunk is mixed and this alone is not evidence of altered entry, antigenicity, or vaccine escape. `S/N` is unchanged versus this close reference.


---

# Pathoplexus Position Frequency Check

Full-length-ish ANDV records only: L >=2100 aa, M >=1100 aa, S >=420 aa. Counts are from translated Pathoplexus latest unaligned nucleotide sequences.

| Segment | Position | Swiss aa | Records | Residue counts | Swiss frequency |
|---|---:|---|---:|---|---:|
| L | 70 | I | 77 | I:67;V:10 | 87.0% |
| L | 144 | R | 77 | R:65;K:11;X:1 | 84.4% |
| M | 193 | A | 141 | A:126;P:9;T:3;M:2;S:1 | 89.4% |
| M | 516 | I | 141 | T:126;K:6;X:4;I:3;F:2 | 2.1% |
| M | 524 | N | 141 | N:128;T:7;X:3;E:2;S:1 | 90.8% |
| M | 930 | N | 141 | N:130;G:9;I:2 | 92.2% |

## Interpretation

- `L70I` is common/consensus-like among full-length records.
- `L144R` is common/consensus-like among full-length records.
- `M193A` is common/consensus-like among full-length records.
- `M516I` is rare in this Pathoplexus full-length set.
- `M524N` is common/consensus-like among full-length records.
- `M930N` is common/consensus-like among full-length records.
## M516I Carrier Records

In the full-length-ish M set, the Swiss residue I516 appears in three 2026 records only in this parse:

| Accession | Country | Date | INSDC |
|---|---|---|---|
| PP_006W6RC.2 | Netherlands | 2026-05-03 | |
| PP_006WBLH.2 | Switzerland | 2026-05-04 | PZ385162.1 |
| PP_006XBKH.1 | France | 2026-05-10 | |

This makes M516I outbreak-associated/rare in the current Pathoplexus full-length M background, but not unique to the Swiss record. It is still not sufficient evidence of altered phenotype without entry/neutralization/replicon data.
