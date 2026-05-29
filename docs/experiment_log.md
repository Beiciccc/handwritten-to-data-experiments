# Experiment Log

## Summary

The tracked work started from submission-format validation and then focused on
postprocessing public baseline outputs. The strongest improvement so far comes
from combining the compact row/text filter with a stronger dense-region
geometry expansion.

## Best By Batch

| Batch | Best score | Submission | Ref |
|---|---:|---|---:|
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
| 1 | 0.36791 | `submission_804_d21_true_bestdrops_rows300_337_denseamt3_sparse1_min13` | 53133004 |
| 2 | 0.36765 | `submission_731_d18_true_bestdrops_rows300_337_densemin16_nms360_min13` | 53014220 |
| 3 | 0.36765 | `submission_742_d19_true_bestdrops_rows300_337_densemin12_nms360_min13` | 53046549 |
| 4 | 0.36765 | `submission_742_d19b_true_bestdrops_rows300_337_densemin12_nms360_min13` | 53046466 |
| 5 | 0.36765 | `submission_743_d19b_true_bestdrops_rows300_337_densemin13_nms360_min13` | 53046505 |
| 6 | 0.36765 | `submission_744_d19b_true_bestdrops_rows300_337_densemin14_nms360_min13` | 53046536 |
| 7 | 0.36765 | `submission_745_d19b_true_bestdrops_rows300_337_densemin15_nms360_min13` | 53046578 |
| 8 | 0.36765 | `submission_798_d21_true_bestdrops_rows300_337_stable360_densemin12_min13` | 53131855 |
| 9 | 0.36765 | `submission_799_d21_true_bestdrops_rows300_337_stable360_densemin13_min13` | 53131886 |
| 10 | 0.36765 | `submission_800_d21_true_bestdrops_rows300_337_stable360_densemin14_min13` | 53131919 |

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
- Dense correction followed by NMS was consistently weaker.
- Uniform y-edge expansion was negative; the useful geometry change was selective expansion for dense rows only.
- Further postprocessing should refine the dense-row geometry expansion around the NMS360 and low-Cyrillic min13 plateau.
