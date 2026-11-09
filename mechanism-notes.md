# v15n-6 analyst verification

Research complete: 8 development evaluator experiments; no invented mechanisms.
Zero sealed submissions. Two frozen-source provisional 20-seed dev nulls.
Best reproduced dev_score: 0.29878340020920335 (v15n-2 actual exp7).
Stopped with no further unclaimed promising committed candidates; no reason to spend remaining budget. Best last improved at experiment 5; 3 experiments since improvement. Budget ceiling 20, not exhausted.

## Ranking and verdicts

| Peer commit | Actual source | dev_score | Era stressed PnL | Verdict / block |
|---|---|---:|---|---|
| v15n-2 ad672fd | 2d2eb5c0, MNQ pre-open 3 contracts /45-point stop | .29878340020920335 | 8697, 9104.25, 645.75 | CONFIRMED; 20-seed p=.4285714286 FAIL; no finalist |
| v15n-3 d09d6e2 | ecfa104a, independently coded MNQ same family | .2982990337831843 | 1746.75, 9381, 1789.5 | CONFIRMED; 20-seed p=.4285714286 FAIL; no finalist |
| v15n-2 41c0db5 | badb2f85, ATR-scaled MNQ | .27110436344509725 | 755.75, 12290.25, -7486.75 | ERA-FRAGILE; risk and year-fraction gates also fail |
| v15n-5 5ec1d2b | 5def630e, ZN extension fade | 0 | -724.375, -791.875, -23.125 | ERA-FRAGILE |
| v15n-5 a73b514 | b2b25557, ES long drift | 0 | -113270, -141532.5, -119352.5 | ERA-FRAGILE |
| v15n-4 bdfa814 | 63a0e195, GC reversal | 0 | -307057.5, -281675, -276057.5 | ERA-FRAGILE |

All metrics, four folds, years, economics, gates, source hashes, and provisional null score arrays recorded in experiments.jsonl. Entries 1-5 and 7 are screens; entries 6 and 8 are null runs. Source root strategy.py retained as exact best reproduced peer source, not modified.

## Mechanism audit

Best v15n-2 source: side from 07:00 open to 09:59 close, fills next minute, holds until 14:30 boundary; 3 MNQ contracts, close-based 45-point stop, per-contract declared risk $90, aggregate entry risk $270. Five PARAMS knobs. Time/side/stop gates below six-gate ceiling. Stop declaration is known before entry; actual close-based exits are not guaranteed intrabar stop fills. No source parameters changed after null.

Best candidate yearly PnL: 2019 -540; 2020 12413.25; 2021 2237.25; 2022 4236.75; 2023 99.75. Positive eras do not erase negative 2019, thin recent era, 2020 concentration, or failed directional evidence. MNQ history begins 2019; no inference of 2010-2018 robustness.

Independent v15n-3 source: signal assignment starts at 10:00 bar (fills 10:01), versus v15n-2 09:59 target; stop anchor also differs (10:00 open versus decision close). These are separate sources, not identical evidence. Its yearly PnL: 2019 -4870.5; 2020 9646.5; 2021 3951; 2022 3229.5; 2023 960.75. MYM loaded for screen/null but untraded. Both tests share evaluator seed schedule; not independent p-values.

## Provenance and corrections

v15n-2 leaderboard 41c0db5 advertised exp3 .2414929 but committed exp5 .2711044; advertised source absent. ad672fd advertised exp6 .2318691 but committed exp7 .2987834; actual exp7 reproduced instead. Exact missing sources requested on feed; not reconstructed.

v15n-3 d09d6e committed ecfa104a differs from logged E9 d960c1ba, but observed E9 metrics reproduce exactly. Initial v15n-6 feed #6809/#6810 incorrectly classified committed source as E13 after reading last log row. Corrected in #6811 and experiment 7 before null; definitive verdict CONFIRMED, null FAIL in #6815. Initial ZN yearly transcription in #6765 corrected in comment #2; experiments.jsonl has correct years.

Evaluator self-check passed on synthetic fixtures. Its bundled self-check exercises a synthetic 200-seed null; no 200-seed development/finalist run and no sealed/OOS data access occurred. One leaderboard submission attempt before commit rejected for uncommitted changes; no evaluator experiment or sealed submission involved.

No finalists recommended. Do not spend sealed slot on these candidates.
