# AlphaGenome-OA Summary Data Companion

This archive accompanies a study benchmarking AlphaGenome-derived RNA variant-effect scores for cis-eQTL gene retrieval across four osteoarthritis tissues. It provides supplementary summary data and supporting documentation.

## Contents

| File or directory | Contents |
| --- | --- |
| `data/Supplementary_Data_Tables_S1-S6.xlsx` | Editable Tables S1-S6, Figure S1 tissue-metric summaries, table index and field dictionary |
| `data/TABLE_INDEX.tsv` | Table index |
| `data/DATA_DICTIONARY.tsv` | Field definitions |
| `supplementary/Supporting_Information.pdf` | Supplementary notes and Figures S1-S2 |
| `supplementary/Supplementary_Notes_and_Table_Legends.pdf` | Supplementary notes and table legends |
| `documentation/` | Source reference, score transformations, rights, data availability and reproducibility limitations |
| `terms/` | Supplied AlphaGenome terms documents and conspicuous usage notice |
| `manifests/SHA256_MANIFEST.tsv` | File-level SHA-256 checksums (excluding the manifest itself) |

## Scientific scope

The workbook reports three non-trained ranking strategies:

- **D0:** genomic proximity, using the negative absolute variant-to-TSS distance as the ranking score.
- **A0:** AlphaGenome-derived RNA_SEQ variant-effect magnitude score.
- **F0:** deterministic equal-rank fusion of D0 and A0, using fixed equal weights and no model fitting.

The primary matched comparison comprises 19,819 variant-tissue queries, 17,767 coordinate-defined locus clusters, 719,368 candidate memberships and 20,202 accepted source-reference-positive relations. These are distinct units.

The reference tissues are low-grade cartilage, high-grade cartilage, synovium and fat pad. The predefined 19-biosample AlphaGenome panel (MSK_PANEL_V1) is heterogeneous and is not a one-to-one representation of the four OA tissues. Supplementary Table S1 describes the biosample panel.

## Source reference

The underlying OA cis-eQTL reference relations are not redistributed. Obtain them from the original study (Katsoula et al., *Nature Communications*, 2026: https://doi.org/10.1038/s41467-026-74993-y) and the Musculoskeletal Knowledge Portal, subject to the source provider's terms. See `documentation/SOURCE_REFERENCE.md`.

## Usage terms and score transformations

AlphaGenome-derived A0 summaries and F0 summaries incorporating A0 are subject to the applicable AlphaGenome Output Terms of Use and AlphaGenome Services Additional Terms. Read `documentation/LICENSES_AND_RIGHTS.md`, `documentation/TERMS_VERSION_AND_APPLICABILITY.md` and the notice in `terms/LEGALLY_BINDING_TERMS_OF_USE.txt` before use. No blanket additional open licence is granted for this archive.

Raw RNA_SEQ scores were converted to absolute magnitudes, summarized by the median across technical replicates within each biosample, and then summarized by the median of the three highest finite biosample-level scores, with the documented fallback rule when the panel lacked finite scores. See `documentation/OUTPUT_MODIFICATIONS.md` for full definitions and the F0 transformation. A0 measures predicted variant-effect magnitude, not baseline expression or causal probability.

The depositor reports individual non-commercial research use. The historical terms version governing each output-generation date has not been independently established; the supplied terms copies are included for reference and notice, not as proof of historical applicability. This material is not for clinical use.

## Scope and limitations

This is a summary-data companion, not a complete end-to-end reproduction package. It excludes raw API responses, prediction caches, full candidate-level score matrices, query-level rank records, model weights, service credentials, individual-level records, fitted-model training artifacts and the complete paper-specific analysis and figure-generation code. See `documentation/REPRODUCIBILITY_LIMITATIONS.md`.

Candidates without accepted source-reference relations are not verified biological negatives. Complete per-tissue source-assayed gene identifier lists were not recovered. Tables S4-S6 report descriptive analyses without new confidence intervals or significance tests. The fixed-query distance-MRR invariance in Table S6 follows from the selected query subset and its positive-distance constraint.

## Access and citation

- GitHub: https://github.com/TMUQIN/alphagenome-oa-summary-data
- Zenodo (archived dataset, v1.0.0): https://doi.org/10.5281/zenodo.24556013
- Concept DOI (all versions): https://doi.org/10.5281/zenodo.24556012

Suggested citation: Qin, D. (2026). *AlphaGenome-OA Summary Data Companion: Benchmarking cis-eQTL Gene Retrieval in Osteoarthritis Tissues* (v1.0.0) [Dataset]. Zenodo. https://doi.org/10.5281/zenodo.24556013

The Zenodo deposit is a fixed publication snapshot. This repository updates the access and citation documentation after publication; the scientific data files and supplementary PDFs are unchanged.

The separate general-purpose Gene Retrieval Validation Toolkit is available at https://doi.org/10.5281/zenodo.24457343. It provides reusable validation utilities, not the full analysis pipeline for this study; its licences do not extend to this data companion.
