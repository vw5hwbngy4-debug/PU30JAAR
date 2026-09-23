# PU30JAAR / BLACKPAPER PU #005 COMPLETE INGEST

Canonical ingest unit for **Power Unlimited issue #005, December 1993**.

This package is the final packaging product of the completed human + machine issue reconstruction.

## Authority order

1. Human visual / reconciled canon
2. Direct issue text
3. Machine structuring / inference
4. External enrichment, not included here

## Final accounting

- 84 physical PDF pages
- 84 page transcript records
- 43 canonical scored evaluations
- 43/43 final scores resolved
- 191 semantic RAG chunks
- 100 issue-grounded entities
- 25 aliases / normalization records
- 61 editor-evidence records
- 46 issue-knowledge records
- 0 external enrichment

## Census equation

The games contents contains 43 platform rows.

`43 - 1 shared Populous II duplicate + 1 ElfQuest board game = 43 scored evaluations`

## Special canon

- Zombies Ate My Neighbors has separate Mega Drive and Super Nintendo scorecards.
- World Heroes 2 is a separate Neo Geo review.
- Populous II has one shared SNES/Mega Drive scorecard.
- ElfQuest has Graphics 8,0 and no printed Geluid component. Do not invent one.
- The Ermac passage is stored as PU's 1993 mystery/report, not retrospective game canon.
- Samurai Shodown reviewer = Kees de Koning.
- Malibu Bikini Volleyball reviewer = René Janssen.

## Files

1. `PU_005_BEST_MACHINE_TRANSCRIPT_FULL.txt`
2. `PU_005_PAGE_TRANSCRIPTS.jsonl`
3. `PU_005_RAG_CHUNKS.jsonl`
4. `PU_005_HUMAN_CANON_REVIEWS.jsonl`
5. `PU_005_ENTITY_INDEX.jsonl`
6. `PU_005_ALIAS_MAP.jsonl`
7. `PU_005_EDITOR_EVIDENCE.jsonl`
8. `PU_005_ISSUE_KNOWLEDGE.jsonl`
9. `PU_005_ISSUE_METADATA.json`
10. `PU_005_PROVENANCE.jsonl`
11. `PU_005_MYSQL_PAGE_UPSERT.sql`
12. `PU_005_RAG_CHUNKS_IMPORT.sql`
13. `PU_005_CONFLICTS.txt`
14. `PU_005_QA_REPORT.txt`
15. `PU_005_INGEST_README.md`

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
