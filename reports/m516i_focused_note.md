# M516I Focused Note - ANDV Swiss 2026

## Question

The only rare outbreak-associated protein difference found in the first Pathoplexus pass is `M/GPC:T516I`. This note asks whether it is technically real, where it sits, and whether the current structural evidence supports a functional or antigenic claim.

## Nucleotide/Codon Support

Across full-length-ish M records in Pathoplexus, codon/residue counts at GPC 516 are:

ACA->T: 71, ACG->T: 55, AAA->K: 5, NNN->X: 4, ATA->I: 3, TTT->F: 2, AAG->K: 1

The `I516` records all use a clean `ATA` isoleucine codon and have zero Pathoplexus ambiguous/unknown M nucleotides in the downloaded metadata:

| Accession | Country | Date | Codon | Ambiguous M | Unknown M | INSDC |
|---|---|---|---|---:|---:|---|
| PP_006W6RC.2 | Netherlands | 2026-05-03 | ATA | 0 | 0 |  |
| PP_006WBLH.2 | Switzerland | 2026-05-04 | ATA | 0 | 0 | PZ385162.1 |
| PP_006XBKH.1 | France | 2026-05-10 | ATA | 0 | 0 |  |


Interpretation: `M516I` is not a translation artifact from an ambiguous codon in these records. In this data pull it is a clean `ACA/ACG` threonine-background to `ATA` isoleucine change in the outbreak-associated records.

## Local Sequence and Hydrophobicity

Reference window versus Swiss/outbreak window around residue 516:

- Reference `PP_006VZ4W.1`, aa 500-530: `PAVTLIILKCLRVLTFSCSHYTNESKFKF`
- Swiss 2026, aa 500-530: `PAVTLIILKCLRVLIFSCSHYTNESKFKF`

Hydrophobicity windows around 516:

| Window | Reference KD | Swiss KD | Delta |
|---|---:|---:|---:|
| 507-525 | 0.5 | 0.774 | 0.274 |
| 502-530 | 0.483 | 0.662 | 0.179 |
| 497-535 | 0.777 | 0.91 | 0.133 |


Interpretation: T->I increases local hydrophobicity, but the absolute KD averages are not enough by themselves to define a new transmembrane segment. It is better read as a local hydrophobicity increase inside/near a pre-existing hydrophobic glycoprotein region.

## AlphaFold Evidence

The top-ranked AlphaFold model covering residue 516 is `andv_swiss_2026_m_glycoprotein_precursor_chunk02_aa351_800`. At GPC 516, CA pLDDT is `79.81`.

The broader AlphaFold context is mixed: chunk02 (`aa351-800`) has low global pTM (`0.43`) despite reasonable local pLDDT around many residues. So residue-level placement near 516 is moderately useful, but the global arrangement of this chunk should not be overinterpreted.

## Experimental Structure Context

The public ANDV Gn-Gc tetramer/Fab structure `9P3Y` includes the Gn sequence carrying the reference `T516`, but the resolved Gn coordinates cover approximately residues 20-479 for the Gn chains. Residue 516 is therefore present in the construct sequence but not resolved in the coordinate model we downloaded from RCSB.

Interpretation: this supports caution. `M516I` is not in a well-resolved exposed region of the available tetramer coordinates; it lies in a membrane-proximal/unresolved part of Gn in that structure.

## Bottom Line

`M516I` is the right mutation to flag:

- rare in the Pathoplexus full-length M background (`I` at 516 in 3/141 full-length-ish M records)
- clean codon support (`ATA`) in the 2026 carrier records
- shared by Netherlands/Switzerland/France 2026 records, so outbreak-associated but not Swiss-unique
- local hydrophobicity increases versus the common `T516` background
- near the `N524` glycosylation motif and the `485-521` hydrophobic region from our sequence scan

But the current evidence does **not** justify a phenotype claim. The strongest defensible wording is: `M516I is a rare, clean, outbreak-associated glycoprotein substitution in a membrane-proximal/unresolved Gn region; it deserves expert structural/entry review, but AlphaFold plus public sequence data do not establish altered entry, transmissibility, antigenicity, or vaccine escape.`

## Follow-up If We Continue

The next useful analysis would be to align this region against the 2026 Cell structure sequence and older ANDV/SNV/HTNV glycoprotein references, then ask whether residue 516 maps to a known Gn stem/TM/cytoplasmic-tail boundary or processing/trafficking determinant. The necessary wet-lab test would be pseudovirus/VLP incorporation and entry/neutralization comparison for T516 versus I516.
