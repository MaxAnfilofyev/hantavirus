# Public-data methods

## Sequence translation

The local Swiss 2026 FASTA contains three ANDV genome segments: `L`, `M`, and
`S`. For each segment, open reading frames were detected by translating all
three forward frames and selecting the longest methionine-starting ORF.

The resulting protein lengths were:

- `L`: 2153 aa
- `M/GPC`: 1138 aa
- `S/N`: 428 aa

The single ambiguous nucleotide in the local `L` segment translated
unambiguously as glutamine because the codon was `CAR`.

## Pathoplexus pull

Pathoplexus data were pulled from the ANDV LAPIS API:

- metadata: `https://lapis.pathoplexus.org/andv/sample/details`
- latest unaligned nucleotide FASTA:
  `https://lapis.pathoplexus.org/andv/sample/unalignedNucleotideSequences?versionStatus=LATEST_VERSION`

Pathoplexus nucleotide records were translated with the same ORF finder. For
frequency checks, records were restricted to full-length-ish proteins:

- `L >= 2100 aa`
- `M >= 1100 aa`
- `S >= 420 aa`

For the broader GPC 516 check, residue calls were assigned by translating each
available M segment ORF and aligning the protein to the Swiss full-length M/GPC
sequence. This Swiss-numbered mapping is required because several outbreak
consensus M records are truncated or start-shifted; raw ORF position 516 can
misclassify those records.

## Reference comparison

The first-pass close older reference was `PP_006VZ4W.1`, selected because it was
one of the closest older complete/reference-like Pathoplexus records to the
Swiss 2026 proteins.

## Structure context

RCSB/PDB `9P3Y` was used as the public ANDV Gn-Gc tetramer/Fab structural
reference. The Swiss GPC was compared with the 9P3Y construct sequence extracted
from the mmCIF. The 9P3Y coordinates resolve the Gn chains through roughly GPC
residue 479, so GPC residue 516 is present in the construct sequence but not
resolved in the coordinate model.

AlphaFold Server predictions were used locally for qualitative support only.
Raw AlphaFold Server outputs are not redistributed in this repository.
