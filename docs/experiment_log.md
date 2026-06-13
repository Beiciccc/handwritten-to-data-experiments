# Experiment Log

## Summary

The tracked work started from submission-format validation and then focused on
postprocessing public baseline outputs. The strongest improvement so far comes
from combining a public artifact ensemble with geometry-based duplicate
suppression.

## Best By Batch

| Batch | Best score | Submission | Ref |
|---|---:|---|---:|
| v1.6 public artifact source-aware NMS refinement | 0.82776 | `submission_1174_d36_ensemble_src_uni045_else050` | 53622630 |
| v1.6 public artifact ensemble and NMS refinement | 0.82762 | `submission_1143_d35_ensemble_nms50` | 53617781 |
| v1.6 duplicate-text page-cap refinement | 0.45646 | `submission_1112_d34_dedup_exact_keep2_pagecap10` | 53551252 |
| v1.6 duplicate-text rescue refinement | 0.45563 | `submission_1097_d33r_dedup_exact_keep2` | 53522493 |
| v1.6 source-routing and text-cleaning probes | 0.45187 | `submission_1076_d33_source_university_day25_else_d32best` | 53520977 |
| v1.6 sparse02 asymmetric yedge interaction | 0.45182 | `submission_1021_d30_dense_top10_bottom18_sparse02_densemin14_nms360_min13` | 53444206 |
| v1.6 sparse02 plateau refinement | 0.45182 | `submission_1026_d31_dense_top11_bottom19_sparse02_densemin14_nms360_min13` | 53478944 |
| v1.6 sparse plateau edge recovery | 0.45182 | `submission_1066_d32_dense_top10_bottom18_sparse02_densemin11_nms360_min13` | 53493238 |
| v1.6 bottom-heavy asymmetric yedge refinement | 0.45181 | `submission_980_d29_dense_top11_bottom18_sparse11_densemin14_nms360_min13` | 53407719 |
| v1.6 asymmetric yedge boundary refinement | 0.45174 | `submission_975_d28_dense_top12_bottom17_sparse11_densemin14_nms360_min13` | 53379359 |
| v1.6 yedge8 and yedge9 expansion | 0.45153 | `submission_888_d25_denseamt9_sparse1_densemin14_nms360_min13` | 53272035 |
| v1.6 yedge10-13 plateau refinement | 0.45153 | `submission_901_d26_denseamt10_sparse0_densemin14_nms360_min13` | 53313246 |
| v1.6 yedge14-16 boundary refinement | 0.45153 | `submission_926_d27_denseamt14_sparse1_densemin14_nms360_min13` | 53344951 |
| v1.6 yedge6 expansion refinement | 0.40377 | `submission_866_d24_denseamt7_sparse1_densemin15_nms360_min13` | 53237101 |
| v1.6 yedge5 and asymmetry refinement | 0.37991 | `submission_832_d23_denseamt5_sparse1_densemin16_nms360_min13` | 53205029 |
| v1.6 dense-edge expansion refinement | 0.37592 | `submission_817_d22_denseamt4_sparse1_densemin16_nms360_min13` | 53149629 |
| v1.6 left-NMS and dense-edge probes | 0.36791 | `submission_804_d21_true_bestdrops_rows300_337_denseamt3_sparse1_min13` | 53133004 |
| v1.6 low-minimum boundary/NMS refinement | 0.36765 | `submission_731_d18_true_bestdrops_rows300_337_densemin16_nms360_min13` | 53014220 |
| v1.6 high-NMS cliff probe | 0.36765 | `submission_742_d19_true_bestdrops_rows300_337_densemin12_nms360_min13` | 53046549 |
| v1.6 NMS360 dense-min rescue | 0.36765 | `submission_742_d19b_true_bestdrops_rows300_337_densemin12_nms360_min13` | 53046466 |
| v1.6 low-Cyrillic minimum refinement | 0.36764 | `submission_686_d17_true_bestdrops_rows300_337_densemin16_min13` | 52977157 |
| v1.6 plateau escape probes | 0.36763 | `submission_776_d20_true_bestdrops_rows300_337_densemin12_nms335_min13` | 53068116 |
| v1.6 dense-min boundary refinement | 0.36671 | `submission_685_d16_true_bestdrops_rows300_337_densemin16_min17` | 52944919 |
| v1.6 compact-window and dense-min refinement | 0.36623 | `submission_662_d15_true_bestdrops_rows300_330_densemin16` | 52911063 |
| v1.6 best-band micro refinement | 0.36583 | `submission_618_d14_true_bestdrops_rows300_330` | 52872132 |
| v1.6 top-band refinement | 0.36490 | `submission_613_d13_bestband_drop203_209_212_239` | 52837063 |
| Top-row low-Cyrillic refinement | 0.36332 | `submission_588_d12b_drop328_plus_rows300_385` | 52792585 |
| v1.5 low-Cyrillic peak refinement | 0.36056 | `submission_539_d11b_adapt_table_lowcyr170_min18_top10rows` | 52724982 |
| Low-Cyrillic text-length sweep | 0.35791 | `submission_448_d10_table_lowcyr20_min18` | 52598441 |
| Table-aware Page CER probes | 0.35689 | `submission_438_d9d_table_lowcyr020_min12` | 52583507 |
| Dense-region and NMS sweep | 0.34393 | `submission_326_d7_nms034_dense18_yedge2` | 52437539 |
| NMS ridge refinement | 0.34392 | `submission_347_d8_nms0334_dense18` | 52495349 |
| Y-edge sweep | 0.34299 | `submission_271_d6_dense18_yedge2_else_best` | 52377852 |
| Combined bbox/postprocess sweep | 0.34097 | `submission_204_d4_peak_yedge_shrink1` | 52336613 |
| Shift and rounding sweep | 0.34012 | `submission_151_tail_x094625_y07535_dy3` | 52270359 |
| Scale-grid sweep | 0.34012 | `submission_211_x94475_y75300_dy3` | 52340128 |
| Anisotropic bbox sweep | 0.33698 | `submission_110_tail_x095_y0755_dy_plus3` | 52226145 |
| Bounding-box refinement | 0.33073 | `submission_057_aniso_x090_y075` | 52209643 |
| Zero-shot output postprocessing | 0.32998 | `submission_041_nms030_shrink080` | 52207621 |
| Initial format probes | 0.11383 | `submission_009_v4_mid_hf` | 52206394 |

## Current Top Submissions

| Rank | Public score | Submission | Ref |
|---:|---:|---|---:|
| 1 | 0.82776 | `submission_1174_d36_ensemble_src_uni045_else050` | 53622630 |
| 2 | 0.82771 | `submission_1156_d36_ensemble_nms490` | 53621315 |
| 3 | 0.82766 | `submission_1166_d36_ensemble_nms500_keep_bottom` | 53622227 |
| 4 | 0.82762 | `submission_1143_d35_ensemble_nms50` | 53617781 |
| 5 | 0.82761 | `submission_1155_d36_ensemble_nms480` | 53621287 |
| 6 | 0.82757 | `submission_1153_d36_ensemble_nms460` | 53621227 |
| 7 | 0.82753 | `submission_1152_d36_ensemble_nms450` | 53621189 |
| 8 | 0.82753 | `submission_1154_d36_ensemble_nms470` | 53621257 |
| 9 | 0.82752 | `submission_1165_d36_ensemble_nms500_keep_top` | 53621592 |
| 10 | 0.82751 | `submission_1157_d36_ensemble_nms510` | 53621347 |

## Notes

- Dense-region correction with y-edge adjustment was a stable improvement path.
- NMS before dense correction improved the best public score to `0.34393`.
- The NMS ridge refinement did not beat `0.34393`; its best was `0.34392`.
- The useful NMS threshold region is left of the `0.367+` drop-off, with `0.334` close to the best plateau.
- Table-region Page CER suppression produced the first clear postprocessing improvement beyond the NMS plateau.
- Low-Cyrillic text filtering with a moderate minimum text length improved the tracked best public score to `0.35791`.
- After the v1.5 test-set and metric update, the low-Cyrillic peak moved slightly and improved the tracked best public score to `0.35804`.
- Isolating the strongest low-Cyrillic row set and removing one harmful row improved the tracked best public score to `0.36106`.
- Very broad Latin/digit heuristics and very long minimum-length cutoffs were negative; the useful region was narrower.
- After the v1.6 train cleanup, true row-328 exclusion with the 300-385 top-band region improved the tracked best score.
- Combining the best delete set with explicit row-328 exclusion and a compact 300-330 window improved the tracked best score.
- Compact-window refinement found a stronger 300-337 boundary and a dense-minimum interaction near the 300-330 anchor.
- Combining the compact 300-337 boundary with dense-minimum correction improved the tracked best score.
- Dense-minimum and low-Cyrillic minimum-length interactions improved the tracked best score on the compact and 300-337 windows.
- Lowering the low-Cyrillic minimum text length on the 300-337 dense boundary produced the strongest tracked score.
- NMS360 with the low-Cyrillic min13 filter produced a small tracked best improvement; lower minimum lengths and boundary expansions were negative.
- High-side NMS probes at `0.367+` were negative; NMS360 dense-min variants tied the tracked best but did not improve it.
- On the 300-337 boundary, min13 remained strongest; min12 and min14 were slightly weaker, while 300-335 and 300-342 boundary moves were negative.
- Plateau escape probes did not improve the tracked best; NMS330/335 variants were stable but slightly weaker, and core-drop reversals, row perturbations, and broad type gates were negative.
- Left-side NMS probes were weaker, but increasing the dense-row y-edge expansion while keeping the sparse-row expansion fixed produced a new tracked best.
- Dense-row y-edge expansion remained the strongest postprocessing lever; yedge4 for dense rows with a high dense-count gate produced a large tracked best improvement.
- Increasing dense-row y-edge expansion to five pixels improved the tracked best again; the useful gate stayed narrow around densemin15-16, while asymmetric expansion was weaker.
- Increasing dense-row y-edge expansion to seven pixels improved the tracked best again; densemin15-16 remained the best gate, while tighter gates and asymmetric variants were weaker.
- Dense-row y-edge expansion continued to improve at eight and nine pixels; yedge9 with densemin14 produced the strongest tracked score, while densemin17+ remained sharply negative.
- The yedge10-13 refinement did not improve the tracked best, but showed a broad plateau across densemin12-14 and sparse0/1; NMS359 and text minimum changes were slightly weaker.
- The yedge14-16 boundary refinement also tied the plateau across densemin12-14 and sparse0/1; densemin15 was sharply negative, rows300-336 was weaker, and small x-scale moves tied but did not improve the best.
- Asymmetric y-edge expansion found a new tracked best: top12/bottom17 improved to `0.45174`, while the opposite top17/bottom12 tied the plateau; ceil-in rounding was sharply negative.
- Bottom-heavy asymmetric y-edge refinement improved the tracked best to `0.45181`; top9-12 with bottom17-20 formed the best plateau, while sparse12/sparse21 were sharply negative and NMS355 was slightly weaker.
- Sparse02 interaction on asymmetric y-edge best cells improved the tracked best to `0.45182`; direct top/bottom extrapolation mostly dropped, while densemin13, sortybucket, and floor-out tied but did not improve.
- Sparse02 plateau refinement did not improve beyond `0.45182`; sparse02 widened the best plateau across many top/bottom anchors, while bottom extrapolation stayed weak and densemin12/13, sortybucket, and floor-out only tied.
- Sparse plateau edge recovery did not improve beyond `0.45182`; sparse03 collapsed to the raw-score band, rows300-336 was negative, and densemin11 plus small x/y scale moves only tied.
- Source-routing probes found only a tiny university-specific gain, while raw zero-shot source substitution was sharply negative. Duplicate-text cleanup became the next useful lever: keeping up to two exact duplicates improved the tracked best to `0.45563`, while broader repeated-text deletion was too aggressive.
- Duplicate-text page-cap refinement improved the tracked best to `0.45646`; keep3 was better than keep2, but the strongest variant capped keep2 deletions at 10 regions per page, showing that duplicate-heavy pages still contain some real repeated content.
- A newly available public artifact ensemble reproduced `0.81947` and became the new baseline; source routing showed the main alternate-model gain is on university pages, while archive and dictation should stay on the full-pipeline side.
- Geometry-based NMS over the public artifact ensemble improved the tracked best to `0.82762`; the best tested threshold was near `0.50`, while same-text NMS and the previous exact-duplicate pagecap rule were weaker.
- Fine NMS threshold search improved the tracked best to `0.82776`; the strongest tested variant used a lower threshold on university pages and the prior NMS threshold elsewhere, while source-only and type-only NMS were much weaker.
- Dense correction followed by NMS was consistently weaker.
- Uniform y-edge expansion was negative; the useful geometry change was selective expansion for dense rows only.
- Further postprocessing should refine the dense-row geometry expansion around the NMS360 and low-Cyrillic min13 plateau.
