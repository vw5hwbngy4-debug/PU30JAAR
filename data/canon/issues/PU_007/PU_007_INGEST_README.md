# PU30JAAR / BLACKPAPER PU #007 COMPLETE INGEST

Canonical ingest unit for **Power Unlimited #007, February 1994**.

The magazine identifies this issue as **Nummer 2, Jaargang 2**.

## Authority order

1. Human visual / reconciled canon
2. Direct issue text
3. Machine structuring / inference
4. External enrichment, not included here

## Final accounting

- 84 physical PDF pages
- 84 page transcript records
- 39 canonical scored evaluations
- 39/39 final scores resolved
- 195 semantic RAG chunks
- 103 issue-grounded entities
- 29 aliases / normalization records
- 53 editor-evidence records
- 53 issue-knowledge records
- 0 external enrichment

## Census equation

The printed game/platform index contains 42 rows.

`42 - 1 shared Super Baseball 2020 duplicate - 2 shared Dracula duplicate rows = 39 scored evaluations`

## Special canon

- `Super Baseball 2020` has one shared Super Nintendo / Sega Mega Drive scorecard.
- `Dracula` has one shared Sega Mega Drive / Super Nintendo / Game Boy scorecard.
- `Dragon Strike` has no printed Graphics or Geluid score components.
- `Terminator 2: Rampage` = Graphics 9,0 / Geluid 8,0 / final 9.
- `NBA Jam` pp54-55 is an unscored secondary ProCheck, not a second scored review.
- `Cliffhanger` Action Replay code = `7E061F03`.
- Adjacent Plastic Ware material on the Sonic Chaos page is not a separate scored evaluation.

## Files

1. `PU_007_BEST_MACHINE_TRANSCRIPT_FULL.txt`
2. `PU_007_PAGE_TRANSCRIPTS.jsonl`
3. `PU_007_RAG_CHUNKS.jsonl`
4. `PU_007_HUMAN_CANON_REVIEWS.jsonl`
5. `PU_007_ENTITY_INDEX.jsonl`
6. `PU_007_ALIAS_MAP.jsonl`
7. `PU_007_EDITOR_EVIDENCE.jsonl`
8. `PU_007_ISSUE_KNOWLEDGE.jsonl`
9. `PU_007_ISSUE_METADATA.json`
10. `PU_007_PROVENANCE.jsonl`
11. `PU_007_MYSQL_PAGE_UPSERT.sql`
12. `PU_007_RAG_CHUNKS_IMPORT.sql`
13. `PU_007_CONFLICTS.txt`
14. `PU_007_QA_REPORT.txt`
15. `PU_007_INGEST_README.md`

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
