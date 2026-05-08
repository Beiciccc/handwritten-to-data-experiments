# Experiment Log

## Summary

The tracked work started from submission-format validation and then focused on
postprocessing public baseline outputs. The strongest improvement so far comes
from applying non-maximum suppression before dense-region geometry adjustment.

## Best By Batch

| Batch | Best score | Submission | Ref |
|---|---:|---|---:|
| Dense-region and NMS sweep | 0.34393 | `submission_326_d7_nms034_dense18_yedge2` | 52437539 |
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
| 1 | 0.34393 | `submission_326_d7_nms034_dense18_yedge2` | 52437539 |
| 2 | 0.34393 | `submission_329_d7_nms035_dense18_yedge2` | 52437586 |
| 3 | 0.34393 | `submission_332_d7_nms036_dense18_yedge2` | 52437956 |
| 4 | 0.34389 | `submission_323_d7_nms032_dense18_yedge2` | 52437451 |
| 5 | 0.34366 | `submission_333_d7_nms036_dense20_yedge2` | 52437983 |
| 6 | 0.34365 | `submission_327_d7_nms034_dense20_yedge2` | 52437549 |
| 7 | 0.34365 | `submission_330_d7_nms035_dense20_yedge2` | 52437616 |
| 8 | 0.34364 | `submission_331_d7_nms036_dense16_yedge2` | 52437917 |
| 9 | 0.34363 | `submission_325_d7_nms034_dense16_yedge2` | 52437511 |
| 10 | 0.34363 | `submission_328_d7_nms035_dense16_yedge2` | 52437567 |

## Notes

- Dense-region correction with y-edge adjustment was a stable improvement path.
- NMS before dense correction improved the best public score to `0.34393`.
- Dense correction followed by NMS was consistently weaker.
- Wide/tall geometry-only rules were negative in the latest batch.
- The next useful sweep is a finer NMS threshold grid around `0.33-0.37` with dense18.
