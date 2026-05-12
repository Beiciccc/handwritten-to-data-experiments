# Experiment Log

## Summary

The tracked work started from submission-format validation and then focused on
postprocessing public baseline outputs. The strongest improvement so far comes
from applying non-maximum suppression before dense-region geometry adjustment.

## Best By Batch

| Batch | Best score | Submission | Ref |
|---|---:|---|---:|
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
| 1 | 0.35689 | `submission_438_d9d_table_lowcyr020_min12` | 52583507 |
| 2 | 0.35659 | `submission_437_d9d_table_lowcyr020_min10` | 52582813 |
| 3 | 0.35597 | `submission_440_d9d_table_lowcyr010_min8` | 52583831 |
| 4 | 0.35594 | `submission_439_d9d_table_lowcyr015_min8` | 52583793 |
| 5 | 0.35584 | `submission_432_d9c_table_lowcyr020_min8` | 52578947 |
| 6 | 0.35441 | `submission_436_d9d_table_lowcyr020_min6` | 52582261 |
| 7 | 0.34964 | `submission_431_d9c_table_lowcyr020_min4` | 52578909 |
| 8 | 0.34943 | `submission_427_d9c_table_lowcyr010` | 52578771 |
| 9 | 0.34940 | `submission_428_d9c_table_lowcyr015` | 52578810 |
| 10 | 0.34931 | `submission_433_d9c_best036_table_lowcyr020` | 52578999 |

## Notes

- Dense-region correction with y-edge adjustment was a stable improvement path.
- NMS before dense correction improved the best public score to `0.34393`.
- The NMS ridge refinement did not beat `0.34393`; its best was `0.34392`.
- The useful NMS threshold region is left of the `0.367+` drop-off, with `0.334` close to the best plateau.
- Table-region Page CER suppression produced the first clear postprocessing improvement beyond the NMS plateau.
- Dense correction followed by NMS was consistently weaker.
- Wide/tall geometry-only rules were negative in the latest batch.
- Further postprocessing should isolate table-region cases and avoid broad printed-text suppression.
