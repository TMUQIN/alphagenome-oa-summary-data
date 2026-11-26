# AlphaGenome output modifications used in the manuscript

The manuscript used the original AlphaGenome model and a frozen RNA_SEQ scoring configuration (`alphagenome==0.7.0`, `ModelVersion.ALL_FOLDS`, `GeneMaskLFCScorer`). No AlphaGenome 2 predictions are included.

The published RNA_SEQ score is a modified summary of the original Output:

1. Raw RNA_SEQ variant-effect scores were converted to absolute magnitudes (`abs(raw_score)`). This removes the predicted direction.
2. Within each biosample, technical replicates were summarized by their median.
3. For each candidate gene, the three largest finite biosample-level absolute scores from the predefined 19-biosample MSK_PANEL_V1 were selected and summarized by their median.
4. When no finite value was available from the predefined panel, the same top-three median rule was applied to all available finite RNA_SEQ biosample scores.
5. Larger final values ranked first.

The resulting quantity is a predicted variant-effect magnitude. It is not baseline gene expression, a causal probability, or a calibrated probability of gene causality. The 19-biosample panel is heterogeneous and is not a one-to-one representation of the four OA tissues. The frozen response archive did not contain quantile scores; no track-calibrated reranking was performed.

For F0, within-query D0 and A0 ranks were normalized as `(n - rank) / (n - 1)` for candidate sets with more than one gene. F0 was the arithmetic mean of the two normalized ranks, using fixed equal weights and no model fitting. F0 therefore remains an Output Derivative because it incorporates A0.

D0 ranked candidates by `-|variant position - TSS position|`, with closest TSS first and exact ties resolved by ascending unversioned Ensembl gene identifier.

No raw API responses, complete candidate-level score matrices, full query-level prediction records or API caches are included in this archive.
