# AlphaGenome-OA Summary Data Companion (V3.9.5)

**Status: local release candidate; not yet published.**

This archive accompanies the GPB AlphaGenome-OA manuscript author-review version V3.9.5. It is a **summary-data companion**, not a complete end-to-end reproduction package.

## Contents

- `data/Supplementary_Data_Tables_S1-S6_V3_9_5.xlsx`: editable workbook containing Supplementary Tables S1-S6, the 20-row Figure S1 tissue-metric source table, a table index, a read-me sheet and a field dictionary.
- `data/TABLE_INDEX.tsv` and `data/DATA_DICTIONARY.tsv`: plain-text exports of the workbook index and field dictionary.
- `supplementary/Supporting_Information_V3_9_5.pdf`: supplementary notes and Supplementary Figures S1-S2.
- `supplementary/Supplementary_Notes_and_Table_Legends_V3_9_5.pdf`: supplementary notes and table legends.
- `terms/`: the two AlphaGenome terms documents supplied for this project and the required conspicuous notice.
- `documentation/`: data scope, score-modification and licensing explanations, and a manuscript availability-statement draft.
- `manifests/SHA256_MANIFEST.tsv`: file-level SHA-256 checksums.

## Scientific scope

The workbook reports frozen summary results for three non-trained strategies:

- **D0:** genomic proximity, using the negative absolute variant-to-TSS distance as the ranking score.
- **A0:** the frozen AlphaGenome RNA_SEQ variant-effect magnitude score.
- **F0:** deterministic equal-rank fusion of D0 and A0, using fixed equal weights and no model fitting.

The matched primary comparison contains 19,819 variant-tissue queries, 17,767 coordinate-defined locus clusters, 719,368 candidate memberships and 20,202 accepted source-reference-positive relations. These are distinct units and should not be interchanged.

Supplementary Table S1 is the 19-biosample MSK_PANEL_V1 manifest. It is **not** the removed `S1_RAW_MAGNITUDE_LINEAR` analysis. Tables S1-S6 are included as manuscript supplementary material; no F1 or S1 training artifacts are included.

The four OA reference tissues are low-grade cartilage, high-grade cartilage, synovium and fat pad. The 19-biosample AlphaGenome panel is heterogeneous and is not a one-to-one match to those four OA tissues.

## AlphaGenome-derived information and required notice

The A0 summary values and the F0 summaries that incorporate A0 are AlphaGenome Output Derivatives. They are distributed only subject to the applicable AlphaGenome terms. The required notice is provided in `terms/LEGALLY_BINDING_TERMS_OF_USE.txt`; the supplied terms documents are included in `terms/`.

The score modifications used in the manuscript are documented in `documentation/OUTPUT_MODIFICATIONS.md`. In brief, raw RNA_SEQ variant-effect scores were converted to absolute magnitudes, summarized by the median across technical replicates within each biosample, and the three largest finite biosample-level values were summarized by their median. The absolute-value transformation removes predicted direction. The resulting score is a predicted variant-effect magnitude, not baseline expression and not a causal probability.

The supplied Output Terms PDF states that the version effective on the date a relevant Output was generated applies. The historical version applicable to every archived output-generation date has **not** been independently established here. The supplied copies are included for transparency and must not be represented as proof of the historical governing version.

This archive is intended only for use consistent with the applicable AlphaGenome terms, including non-commercial-use, organizational eligibility, conspicuous-notice and modification-disclosure requirements. It is not for clinical use. The depositor must confirm that the original API use and any organizational authorization satisfy the applicable terms before public release.

## What is not included

This archive does not include:

- raw AlphaGenome API responses or prediction caches;
- the complete variant-by-candidate prediction matrix;
- raw candidate-level prediction-score tables or full query-level rank records;
- model weights, service credentials or restricted individual-level records;
- F1 grouped-pairwise ranker or `S1_RAW_MAGNITUDE_LINEAR` training data, fitted models, coefficients or out-of-fold predictions;
- the complete paper-specific D0/A0/F0 analysis and figure-generation code;
- unresolved main-figure artwork or main-figure source files.

The general-purpose **Gene Retrieval Validation Toolkit v0.1.0** is a separate software product at https://doi.org/10.5281/zenodo.24457343. It provides reusable validation utilities; it does not contain this paper's full analysis pipeline and cannot independently reproduce all manuscript results.

The source OA cis-eQTL reference relations are not redistributed here. See Katsoula et al., *Nature Communications* (2026), DOI: https://doi.org/10.1038/s41467-026-74993-y, and the Musculoskeletal Knowledge Portal for source access.

## Interpretation limits

Candidates without an accepted source-reference relation are not verified biological negatives. The complete per-tissue source-assayed gene identifier lists were not recovered for this benchmark. Tables S4-S6 are descriptive post-primary analyses; no new confidence intervals or inferential tests were generated for those tables. The fixed-query distance-MRR invariance in Table S6 follows from the selected query subset and its positive-distance constraint.

## Citation

Cite the associated manuscript and, after publication, cite the versioned repository/Zenodo record. The general-purpose toolkit should be cited separately using its own DOI above. No paper-specific DOI or public repository URL has been assigned to this local candidate.
