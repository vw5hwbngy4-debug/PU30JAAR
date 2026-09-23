# PU 1993 YEAR_INTELLIGENCE v1

`ISSUE_INGEST → YEAR_SYNTHESIS → YEAR_INTELLIGENCE`

This package compiles deterministic runtime intelligence above the five intact 1993 issue units. It does not replace them.

## Primary runtime products
- `1993_REVIEWER_STATS.json`
- `1993_GAME_RANKINGS.json`
- `1993_PLATFORM_STATS.json`
- `1993_SCORE_DISTRIBUTION.json`
- `1993_CROSS_ISSUE_ARCS.jsonl`
- `1993_READER_FEEDBACK.jsonl`
- `1993_EDITOR_CONTINUITY.jsonl`
- `1993_EMULATOR_UPDATES.jsonl`
- `1993_EMULATOR_CANDIDATES.jsonl`
- `1993_RUNTIME_GOLD_QUESTIONS.jsonl` (160 questions)
- `1993_META_RAG_CHUNKS.jsonl`

## Additional products
- `1993_REVIEWER_BEHAVIOR.jsonl`
- `1993_ANOMALIES.jsonl`
- `1993_GAME_TRENDS.json`
- `1993_PU_CULTURE.jsonl`
- `1993_RUNTIME_ROUTES.json`
- `1993_YEAR_INTELLIGENCE_REPORT.md`
- `SOURCE_REGISTER.json`
- `QA_REPORT.json`

## Hard rules
1. Issue human canon remains authority for review identity, reviewer, score and report fields.
2. No platform score merging.
3. Original 10-point scale preserved.
4. `Michael Schaefer`/`Michael Schaeffer` is only grouped in derived year statistics and is explicitly marked as inference.
5. Emulator candidates are evidence-gated. Assignment frequency and scores are not psychology.
6. No external knowledge used.
