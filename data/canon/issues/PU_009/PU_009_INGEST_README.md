# PU30JAAR / BLACKPAPER PU #009 COMPLETE INGEST

Canonical ingest unit for **Power Unlimited #009, April 1994**.

Factory label: **Nummer 4, Jaargang 2**.

## Final accounting

- 84/84 physical pages
- 35/35 canonical scored evaluations
- 35/35 final scores resolved
- 199 semantic RAG chunks
- 106 entities
- 50 aliases
- 47 editor-evidence records
- 64 issue-knowledge records
- 587 provenance records
- 0 external enrichment

## Structural QA repair

Final packaging caught a non-factual defect in `CANON_KNOWLEDGE_BUILD_v1`: all 35 review records accidentally shared the same record ID.

`CANON_KNOWLEDGE_BUILD_v1.1` repairs this to unique IDs `PU_009_REVIEW_001` through `PU_009_REVIEW_035`.

No score, reviewer, title, platform, verdict or issue-knowledge fact changed.

## Intentional unresolved reviewers

- Zool
- Seek & Destroy
- Nigel Mansell's World Championship

## Source/canon distinction

`De Smurfen` keeps printed platform `GAME SMURF`, with separate canonical platform `Game Boy`.

## Final-only scorecards

No Graphics/Geluid components are invented for:
- Lost Dimensions
- Super Battle Tank 2
- Daffy Duck: The Marvin Missions
- NBA Jam

## Files

1. `PU_009_BEST_MACHINE_TRANSCRIPT_FULL.txt`
2. `PU_009_PAGE_TRANSCRIPTS.jsonl`
3. `PU_009_RAG_CHUNKS.jsonl`
4. `PU_009_HUMAN_CANON_REVIEWS.jsonl`
5. `PU_009_ENTITY_INDEX.jsonl`
6. `PU_009_ALIAS_MAP.jsonl`
7. `PU_009_EDITOR_EVIDENCE.jsonl`
8. `PU_009_ISSUE_KNOWLEDGE.jsonl`
9. `PU_009_ISSUE_METADATA.json`
10. `PU_009_PROVENANCE.jsonl`
11. `PU_009_MYSQL_PAGE_UPSERT.sql`
12. `PU_009_RAG_CHUNKS_IMPORT.sql`
13. `PU_009_CONFLICTS.txt`
14. `PU_009_QA_REPORT.txt`
15. `PU_009_INGEST_README.md`
