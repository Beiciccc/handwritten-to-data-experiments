# Final Report

## Result

- Competition status: Completed
- Online stage end: `2026-06-15 20:59:00 UTC`
- Team: `Kun Zhang`
- Final rank: `36/199`
- Final leaderboard score: `0.82792`
- Leaderboard snapshot: `2026-06-17 12:02:07 UTC`

## Top-Scoring Submissions

| Public score | Submission | Ref | Submitted |
|---:|---|---:|---|
| 0.82792 | `submission_1214_d38_src_u450_s500_a480_d520` | 53694476 | 2026-06-15T03:16:59.673Z |
| 0.82792 | `submission_1221_d38_src_u450_s500_a480_d530` | 53695588 | 2026-06-15T04:03:53.303Z |

The repository includes the tied top-scoring generated CSV files under
`best_submissions/`.

## Summary

The largest gain came from using a public artifact ensemble as the base and
then applying source-aware geometry-based duplicate suppression. The final
refinement kept archive suppression near `0.48` while loosening dictation
suppression to the `0.52-0.53` range.
