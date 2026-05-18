# Experiment Log

## Summary

The tracked work started from submission-format validation and then focused on
postprocessing public baseline outputs. The strongest improvement so far comes
from applying non-maximum suppression before dense-region geometry adjustment.

## Best By Batch

| Batch | Best score | Submission | Ref |
|---|---:|---|---:|
| Top-row low-Cyrillic refinement | 0.36106 | `submission_549_d12_top10_drop328_lowcyr170_min18` | 52764893 |
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
| 1 | 0.36106 | `submission_549_d12_top10_drop328_lowcyr170_min18` | 52764893 |
| 2 | 0.36097 | `submission_544_d12_top10_drop209_lowcyr170_min18` | 52764738 |
| 3 | 0.36097 | `submission_545_d12_top10_drop212_lowcyr170_min18` | 52764772 |
| 4 | 0.36087 | `submission_541_d12_top10_drop203_lowcyr170_min18` | 52764648 |
| 5 | 0.36086 | `submission_546_d12_top10_drop239_lowcyr170_min18` | 52764806 |
| 6 | 0.36076 | `submission_551_d12_top10_add384_lowcyr170_min18` | 52764956 |
| 7 | 0.36056 | `submission_539_d11b_adapt_table_lowcyr170_min18_top10rows` | 52724982 |
| 8 | 0.36049 | `submission_561_d12_top10_lowcyr170_min17` | 52766282 |
| 9 | 0.36047 | `submission_553_d12_top10_add265_lowcyr170_min18` | 52765016 |
| 10 | 0.36045 | `submission_537_d11b_adapt_table_lowcyr170_min18_rows250_385` | 52724929 |

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
- Dense correction followed by NMS was consistently weaker.
- Wide/tall geometry-only rules were negative in the latest batch.
- Further postprocessing should isolate the moderate-length low-Cyrillic region and avoid broad printed-text suppression.
