# Reproducibility and data-scope limitations

This is a summary-data companion, not a complete reproduction package.

Included:
- editable Supplementary Tables S1-S6;
- the workbook's Figure S1 tissue-metric source table;
- Supplementary Figures S1-S2 and their associated notes;
- a data dictionary and explicit description of the score transformations;
- the supplied AlphaGenome terms documents and required notice.

Not included:
- raw AlphaGenome API responses, model outputs or prediction caches;
- complete variant-by-candidate score matrices, candidate-level raw scores or query-level ranks;
- the full paper-specific analysis and figure-generation scripts;
- the complete source OA eQTL reference tables;
- F1/S1 training artifacts or any fitted/OOF model material.

Consequently, a reader can inspect the reported supplementary summary results and their definitions, but cannot reconstruct every query-level or candidate-level metric from this archive alone. The generic Gene Retrieval Validation Toolkit DOI is not a substitute for the missing paper-specific pipeline.

The source study's complete per-tissue tested-gene identifiers were not recovered. Candidates without an accepted source relation are not verified biological negatives. Tissue-stratified and nested-window results in Tables S4-S6 are descriptive; no new subgroup confidence intervals or significance tests were generated.
