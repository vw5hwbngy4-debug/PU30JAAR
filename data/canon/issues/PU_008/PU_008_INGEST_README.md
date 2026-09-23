# PU30JAAR / BLACKPAPER PU #008 COMPLETE INGEST

Canonical ingest unit for **Power Unlimited #008, March 1994**.

The magazine identifies this issue as **Nummer 3, Jaargang 2**.

## Authority order

1. Human visual / reconciled canon
2. Direct issue text
3. Machine structuring / inference
4. External enrichment, not included here

## Final accounting

- 84 physical PDF pages
- 84 page transcript records
- 40 canonical scored evaluations
- 40/40 final scores resolved
- 196 semantic RAG chunks
- 106 issue-grounded entities
- 32 aliases / normalization records
- 52 editor-evidence records
- 52 issue-knowledge records
- 0 external enrichment

## Census equation

The printed `Spellen` contents contains 40 game/platform rows.

`40 - 1 shared Ottifants duplicate + 1 Magic card game outside Spellen = 40 scored evaluations`

## Intentional unresolved reviewer fields

The archive does **not** guess the reviewers of:
- `Mean Arenas`
- `Arabian Nights`

Their scorecards are canonical and fully scored, but the reviewer/byline is not visibly reliable enough to assign.

## Special canon

- `Ottifants` has one shared Sega Mega Drive / Game Gear scorecard.
- `Magic` has Graphics 9, printed Geluid `n.v.t.`, final 9.
- `Pink Goes to Hollywood` = 7,9.
- `Steel Machine` = 8,8.
- `Microcosm` = 7,3.
- `Flight Sim Toolkit` Graphics = 7,9.

## Files

1. `PU_008_BEST_MACHINE_TRANSCRIPT_FULL.txt`
2. `PU_008_PAGE_TRANSCRIPTS.jsonl`
3. `PU_008_RAG_CHUNKS.jsonl`
4. `PU_008_HUMAN_CANON_REVIEWS.jsonl`
5. `PU_008_ENTITY_INDEX.jsonl`
6. `PU_008_ALIAS_MAP.jsonl`
7. `PU_008_EDITOR_EVIDENCE.jsonl`
8. `PU_008_ISSUE_KNOWLEDGE.jsonl`
9. `PU_008_ISSUE_METADATA.json`
10. `PU_008_PROVENANCE.jsonl`
11. `PU_008_MYSQL_PAGE_UPSERT.sql`
12. `PU_008_RAG_CHUNKS_IMPORT.sql`
13. `PU_008_CONFLICTS.txt`
14. `PU_008_QA_REPORT.txt`
15. `PU_008_INGEST_README.md`

## Recommended ingest order

1. metadata
2. page transcripts
3. raw page upsert
4. human review canon
5. entities
6. aliases
7. editor evidence
8. issue knowledge
9. RAG chunks
10. RAG SQL import
11. provenance
12. QA

The original magazine scan remains final evidence for what was printed.
