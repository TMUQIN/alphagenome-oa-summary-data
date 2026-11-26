# Build report - AlphaGenome-OA Summary Data Companion v1.0.0

Status: Public GitHub repository snapshot; no versioned GitHub Release or Zenodo deposit has been created yet.

Source: `E_AlphaGenome_OA_GPB_V3_9_5_LOW_RISK_AUTHOR_REVIEW.zip`, submission workbook and supplementary PDFs; user-supplied AlphaGenome Output Terms and Services Additional Terms PDFs.

Actions performed:
- Copied the V3.9.5 supplementary workbook into a public-facing copy.
- Replaced the internal project-path provenance string in the workbook Read_me sheet with a path-free provenance description. All other workbook table content was retained.
- Exported the workbook table index and field dictionary to TSV.
- Copied the V3.9.5 Supporting Information and Supplementary Notes/Table Legends PDFs.
- Included the two user-supplied AlphaGenome terms PDFs and the exact conspicuous notice from the supplied Services Additional Terms.
- Wrote scope, score-modification, licensing, terms-version and reproducibility documentation.

Validation:
- Workbook opens successfully with openpyxl.
- Expected 10 visible worksheets are present: Index_of_Tables, Read_me, Table_S1_MSK_panel, Table_S2_Eligibility, Table_S3_MRR_crosswalk, Table_S4_Figure2D, Table_S5_Window, Table_S6_Fixed_query, Figure_S1_Tissue_metrics, Field_Dictionary.
- Supplementary Tables S1-S6 are present. Table S1 is the biosample manifest and is distinct from the removed S1_RAW_MAGNITUDE_LINEAR analysis.
- Workbook contains no external links, macros or formulas.
- The sole internal workspace path identified in workbook text was removed from the public-facing copy.
- No raw API responses, complete candidate-level score matrix, full query-level rank records, F1/S1 training artifacts or credentials were included.
- SHA-256 manifest generated for all files except the manifest itself.

Limitations / outstanding author checks:
- No paper-specific D0/A0/F0 analysis scripts were found in the reviewed V3.9.5 submission package; none were invented or included.
- The complete historical AlphaGenome terms version applicable to each output-generation date was not established.
- The depositor reports individual non-commercial use of AlphaGenome Services. Historical terms applicability to each output-generation date has not been independently established. Source-data rights and final author approval remain author-side responsibilities.
- This package is a summary-data companion, not a complete reproducibility archive.
- The repository was created as public and the 17-file candidate was pushed to its main branch. No GitHub Release, Zenodo deposit or versioned DOI has yet been created.
