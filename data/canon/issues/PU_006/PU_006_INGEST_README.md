# PU30JAAR / BLACKPAPER PU #006 COMPLETE INGEST

Canonical ingest unit for **Power Unlimited #006, January 1994**.

The magazine identifies this issue as **Nummer 1, Jaargang 2**.

## Authority order

1. Human visual / reconciled canon
2. Direct issue text
3. Machine structuring / inference
4. External enrichment, not included here

## Final accounting

- 84 physical PDF pages
- 84 page transcript records
- 36 canonical scored evaluations
- 36/36 final scores resolved
- 183 semantic RAG chunks
- 98 issue-grounded entities
- 30 aliases / normalization records
- 50 editor-evidence records
- 48 issue-knowledge records
- 0 external enrichment

## Census equation

The printed game/platform index contains 37 rows.

`37 - 1 unscored CD-i Full Motion Video feature - 1 shared Lethal Enforcers platform duplicate + 1 History of the World board game = 36 scored evaluations`

## Special canon

- `CD-i Full Motion Video` p53 is an unscored Power Pro feature.
- `Lethal Enforcers` has one shared Sega CD / Mega Drive scorecard, directly attributed to Michael + Kees.
- `History of the World` has no printed Graphics or Geluid score components.
- `Oscar` is a PREVIEW on p44.
- `Metal & Lace` is on p45; the printed contents swaps the Oscar/Metal & Lace page numbers.
- `Tournament Fighters` has separate Super Nintendo and Mega Drive scorecards.
- `Tom & Jerry: Frantic Antics!` sound = 6,5.
- `RoboCop 3` = Graphics 5,0 / Geluid 5,0 / final 4.

## Files

1. `PU_006_BEST_MACHINE_TRANSCRIPT_FULL.txt`
2. `PU_006_PAGE_TRANSCRIPTS.jsonl`
3. `PU_006_RAG_CHUNKS.jsonl`
4. `PU_006_HUMAN_CANON_REVIEWS.jsonl`
5. `PU_006_ENTITY_INDEX.jsonl`
6. `PU_006_ALIAS_MAP.jsonl`
7. `PU_006_EDITOR_EVIDENCE.jsonl`
8. `PU_006_ISSUE_KNOWLEDGE.jsonl`
9. `PU_006_ISSUE_METADATA.json`
10. `PU_006_PROVENANCE.jsonl`
11. `PU_006_MYSQL_PAGE_UPSERT.sql`
12. `PU_006_RAG_CHUNKS_IMPORT.sql`
13. `PU_006_CONFLICTS.txt`
14. `PU_006_QA_REPORT.txt`
15. `PU_006_INGEST_README.md`

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
